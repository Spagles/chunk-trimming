# chunk-trimming

Cuts chunk writes on Paper servers by saving only chunks a player has visited.

## How it works

Only chunks that were freshly generated and have not been written to disk yet are considered, so anything a world
already holds stays untouched.

Such a chunk will only be saved on unload if a player was within the `save-radius`, or if something they set in motion
reached into it, e.g. pistons, dispensers, falling blocks, explosions, projectiles or spawned entities. Everything else
is skipped and regenerates from the seed on its next load.

You can use `/chunktrimming` to show skipped and kept chunks.

## Downloads

You can download the latest jar file
from [my build server](https://build.florianreuth.de/job/chunk-trimming), [GitHub Actions](https://github.com/florianreuth/chunk-trimming/actions)
or use the [releases tab](https://github.com/florianreuth/chunk-trimming/releases).

## Contact

If you encounter any issues, please report them on the
[issue tracker](https://github.com/florianreuth/chunk-trimming/issues). If you just want to talk or need help with
chunk-trimming, feel free to join my
[Discord](http://florianreuth.de/discord).

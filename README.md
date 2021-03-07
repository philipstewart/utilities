# Random utilities

Small utilities written when I have failed to find a suitable 
alternative when needed.

## cp2exfat

Originally written to copy files from an ext4 filesystem to an exfat 
MicroSDXC card, where the ext4 paths may contain characters which are 
invalid on an exfat filesystem.

```shell
$ cp2exfat -h
usage: cp2exfat [-h] [-n] [--verbosity LEVEL] SRC DST

Recursively copy a directory to an exfat target

positional arguments:
  SRC                source directory
  DST                destination directory

optional arguments:
  -h, --help         show this help message and exit
  -n, --dry-run      simulate, but do not make changes
  --verbosity LEVEL  logging level: CRITICAL,ERROR,[WARNING],INFO,DEBUG
```

Requires Python 3.

n.b. The morning after, it feels like there should be a simpler solution 
to this, either using `rsync` or piping `find SRC -type f` via `tr [-d]` 
to `cp`.

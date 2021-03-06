# Random utilities

Small utilities written if I have failed to find a suitable alternative
when required.

## cp2exfat

Originally written to copy files from an ext4 filesystem to an exfat 
MicroSDXC card where the ext4 paths may contain characters which are 
invalid on an exfat filesystem.

```shell
$ cp2exfat -h
usage: cp2exfat [-h] [--dry-run] [--verbosity LEVEL] SRC DST

Recursively copy a directory to an exfat target

positional arguments:
  SRC                source directory
  DST                destination directory

optional arguments:
  -h, --help         show this help message and exit
  --dry-run, -n      simulate, but do not make changes
  --verbosity LEVEL  logging level: CRITICAL,ERROR,[WARNING],INFO,DEBUG
```

Requires Python 3.
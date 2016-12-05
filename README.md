copy-files-in-parallel
======================

A python wrapper to rsync and parallel to copy a large number files using parallel threads.

Prerequisites
-------------

You need [GNU parallel](http://www.gnu.org/software/parallel/) to run this script. On debian/Ubuntu you should be able to install it using:

```
apt-get install parallel
```

For other systems, please follow the information on (http://www.gnu.org/software/parallel/).

Usage
-----

To copy all files and directories in `foo` to `bar` use:

```
copy-files-in-parallel /path/to/foo /path/to/bar
```
or

```
copy-files-in-parallel /path/to/foo other.machine:/path/to/bar
copy-files-in-parallel other.machine:/path/to/bar /path/to/foo
```

for a copy using ssh.

More information can be found using the `-h`/`--help` option:

```
usage: copy-files-in-parallel [-h] [-j J] [-c C] [--resume RESUME] [--dry]
                              [--lfs] [--arcfour] [--tmp TMP]
                              source destination

Copy files in parallel.

positional arguments:
  source           source path
  destination      destination path

optional arguments:
  -h, --help       show this help message and exit
  -j J             number of threads to use
  -c C             number of files in one chunk
  --resume RESUME  resume previous job (skip finding files)
  --dry            perform a trial run with no changes made
  --lfs            use lustre utilities
  --arcfour        use arcfour as compression algorithm
  --tmp TMP        path to store temporary data
```

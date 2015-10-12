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
```

for a copy using ssh. Please note that trailing slashes are not allowed.

More information can be found using the `-h`/`--help` option:

```
copy-files-in-parallel -h
```

# Goal
The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed.

## What to learn
How to determine file attributes, managing multiple compression utilities, redirecting files within directories, and how to create temporary work spaces.

### Tools of Use
- mktemp -d : make temporary directory
- cp
- file
- bzip2
- gzip
- tar
- xxd

#### Additional Notes:

If you `cat data.txt` you can find the hex output with a file header reading `1f8b`  which a google search and a wiki page later will  give us our first hint. (not the fastest route but still a route)

```bash
gzip = .gz
bzip2 = .bz2
posix = .tar
```

```bash
gunzip foo
bunzip2 foo
tar -xf foo
```
with `tar` `-x` is extract
```bash
TAR_FILETYPE
	Type of the file. It is a single letter with the following meaning:
		f    Regular file
		d    Directory
		l    Symbolic link
		h    Hard link
		b    Block device
		c    Character device
	Currently only regular files are supported.
```
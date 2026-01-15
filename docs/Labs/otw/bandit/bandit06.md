# Goal

Have to find the file with the following properties:
- human-readable
- 1033 bytes in size
- not executable

## What to learn

Learning tool flags to narrow down specific details of file properties.

### Tools to consider
- `find`
### Flags to consider
- -type
- -size 


### Added notes:
- -size operates in binary units with exact measurements.  I was confused as to why the man page stated the following units.
  
  ```bash
	  'b' - 512-byte block
	  'c' - bytes
	  'w' - two-byte words
	  'k' - kibibytes (KiB, units of 1024 bytes)
	  'M' - mebibytes (MiB, 1024 * 1024 = 1048576 bytes)
	  'G' - gibibytes (GiB, 1024^3 = 1073741824 bytes)
  ```
  
	I thought they were new units of measurement, which yes but also no. Instead of the estimated file sizes such as KB being 1000 bytes, KiB is exactly 1024 bytes to stay in line with the exact systems sizes.

- -type the following is a list of the character types that -type can be called
	```bash
	'b' block (buffered) special
	'c' character (unbuffered) special
	'd' directory
	'p' named pipe (FIFO)
	'f' regular file
	'l' symbolic link; never true if -L or -follow option is in effect. if -L is in effect use -xtype
	's' socket
	'D' door (Solaris systems)
	```
# Goal
The password for the next level is the only human-readable file in the `inhere` directory.

## What to learn

How to determine file contents to determine that which is human readable versus random data and machine readable.

### Commands possible to solve this level

-  `file` - %%``` file ./-file**```%%
-  `find` - %%```find . -type f -exec strings {} \;```%%

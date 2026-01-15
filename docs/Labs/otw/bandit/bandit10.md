# Goal
Password is stored in the file `data.txt` and is one of the few human-readable strings, preceded by several "=" characters.


## What to learn
How to filter output based on recognizable patterns.

### Tools of use
- strings
- grep

#### Additional Notes:
```bash
grep "=" file.txt
grep: data.txt: binary file matches
```
- grep may report "binary file matches" if the file contains non-text bytes
- >! use `grep -a` or pipe through `strings` to safely view human-readable content.!<


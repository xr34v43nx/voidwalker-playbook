# Goal
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user `bandit14`. For this level you don't get the next password, but you get a private SSH key that can be used to log into the next level.

## What to learn
How to transfer files between systems and how to use ssh via a key file versus a login password challenge.

### Tools of Use
- scp
- chmod

#### Additional Notes:
scp syntax was not easy for me to get right
```bash
scp -P port user@from_host:file.txt /local/directory/
```
courtesy of OTW using non-standard ssh ports we have to specify the port through a flag for it to work.

chmod is required so the file mode bits can be altered so the file can be somewhat secured? I just know that the ssh would not accept the key unaltered. This specific utility requires it's own dedicated notes down the road.
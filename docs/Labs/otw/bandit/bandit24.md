# Goal
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

# What to Learn
Per the Notes above, we are exploiting setuid and cronjobs in order to allow access to the next password.

```bash
#!/bin/bash
shopt -s nullglob
myname=$(whoami)

cd /var/spool/"$myname"/foo || exit 
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." ] && [ "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" "./$i")"
        if [ "${owner}" = "bandit23" ] && [ -f "$i" ]; then
            timeout -s 9 60 "./$i"
        fi
        rm -rf "./$i"
    fi
done

```

Lets "Step Through" this script.
When it runs it changes the directory to `/var/spool/"$myname"/foo` and then exits
then echos the text. for  i in file . extension;
do
	 if file does not equal current directory and does not equal the previous directory then echo out Handling file, owner equals shell to call the user and run with args and the script in question. if the owner equals bandit23 and file is $i wait 60 seconds and run. finish the execution and then delete the file. Complete the program.
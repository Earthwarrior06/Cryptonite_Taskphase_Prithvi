# Pondering PATH


## The PATH Variable

We can prevent a command from accessing certain commands by setting the PATH variable to ""(null)
```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{gVE7OArDlYPsA4A8LYkRFYWKI15.dZzNwUDL5cDO0czW}
```


## Setting PATH:

We can set the path from which a programme should run by giving a value to the path variable

Here /challenge/run tries to run /challenge/more_commands/win using just win 

So we set the path as /challenge/more_commands/ so that the command works
```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{40lq-mzLze9jbr-YuIpFicA5ptz.dVzNyUDL5cDO0czW}
```


## Adding Comands:
We use "nano" editor to create shell programmes

We use the "mv" command to move shell programmes to another name

```bash
hacker@path~adding-commands:~$ nano win.sh
hacker@path~adding-commands:~$ mv win.sh win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{szHAuAyvmj6JxSNtKgI0lFkmXQT.dZzNyUDL5cDO0czW}
```

## Hijacking Commands:

We first create a fake rm that will be exectuted instead of the real rm command(delete)
```bash
PATH = /run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
cat /flag
```
We move rm.sh to rm using mv

Then we change the path to add "/home/hacker"

We use the "which" command to check from where a certain command will be run from

```bash
hacker@path~hijacking-commands:~$ echo $PATH
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~hijacking-commands:~$ nano rm.sh
hacker@path~hijacking-commands:~$ mv rm.sh rm
hacker@path~hijacking-commands:~$ chmod a+x rm
hacker@path~hijacking-commands:~$ which rm
/run/workspace/bin/rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker:$PATH
hacker@path~hijacking-commands:~$ which rm
/home/hacker/rm
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
/home/hacker/rm: line 1: PATH: command not found
pwn.college{EkulaPnT8j1iSJCQsuixlu_5D6Q.ddzNyUDL5cDO0czW}
```

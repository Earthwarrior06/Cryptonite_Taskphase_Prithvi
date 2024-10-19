# Pondering Path


## The PATH Variable


```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{gVE7OArDlYPsA4A8LYkRFYWKI15.dZzNwUDL5cDO0czW}
```


## Setting PATH:



```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{40lq-mzLze9jbr-YuIpFicA5ptz.dVzNyUDL5cDO0czW}
```


## Adding Comands:


```bash
hacker@path~adding-commands:~$ nano win.sh
hacker@path~adding-commands:~$ ls -l win
ls: cannot access 'win': No such file or directory
hacker@path~adding-commands:~$ ls -l win.sh
-rwxrwxrwx 1 hacker hacker 10 Oct 19 18:14 win.sh
hacker@path~adding-commands:~$ PATH="/home/hacker:$PATH"
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/challenge/run: line 4: win: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:~$ mv win.sh win
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{szHAuAyvmj6JxSNtKgI0lFkmXQT.dZzNyUDL5cDO0czW}
```

##

```bash


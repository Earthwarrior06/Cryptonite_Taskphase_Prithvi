#

## 1.Listing Processes:

We can list out all the processes
```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 17:46 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 17:46 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 17:46 ?        00:00:00 /challenge/10768-run-2625
root          72      68  0 17:46 ?        00:00:00 sleep 6h
hacker        73       0  0 17:46 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        91      73  0 17:47 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/10768-run-2625
Yahaha, you found me! Here is your flag:
pwn.college{4ZkkT9xlGjRiJvjAN8yYukZ5vsa.dhzM4QDL5cDO0czW}
```

## 2.Killing Processes:


```bash
hacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker        73  0.0  0.0   4976  3520 ?        Ss   17:56   0:00 /challenge/dont_run
hacker        97  0.0  0.0   4140  2240 pts/0    S+   17:57   0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{o2p1yyW7tINAdbUNVeX10xE4L0c.dJDN4QDL5cDO0czW}
```

## 3.Interrupting Processes:

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{wK2A_bqmpJyQ3fH3hmahjjNs9mU.dNDN4QDL5cDO0czW}
```

## 4.Suspending Processes:

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 18:03 pts/0    00:00:00 bash /challenge/run
root          84      82  0 18:03 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 18:03 pts/0    00:00:00 bash /challenge/run
root          89      65  0 18:04 pts/0    00:00:00 bash /challenge/run
```

## 5.Resuming Processes:

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{MpK7wXdDyq5ChcdXYlSEdTPgG0y.dZDN4QDL5cDO0czW}
Don't forget to press Enter to quit me!

Goodbye!
```


## 6.Backgrounding Processes:



```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S+   bash /challenge/run
root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S    bash /challenge/run
root          92 S    sleep 6h
root          93 S+   bash /challenge/run
root          95 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{YQMzUkzOn-AsRvlZWy7fQp8jofR.ddDN4QDL5cDO0czW}
```

## 7.Foregrounding Processes



```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{4YVDH_cxbCvmmQ8lptsfJDZe0oM.dhDN4QDL5cDO0czW}
```


## 8.Starting Backgrounded Processes:


```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82



hacker@processes~starting-backgrounded-processes:~$ Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{4r93yvSmGtbZmoTDXAMLOE3O-hU.dlDN4QDL5cDO0czW}
```

## 9.Process Exit Codes:


```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
49
hacker@processes~process-exit-codes:~$ /challenge/submit-code 49
CORRECT! Here is your flag:
pwn.college{MRR6cMtC0cJ9FDlLG7HCHU99-H_.dljN4UDL5cDO0czW}
```


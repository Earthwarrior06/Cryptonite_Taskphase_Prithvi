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

##

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

##

```bash
root          91      89  0 18:04 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{AKklWUd8C7pgxWtgWV1Aw9UKoRR.dVDN4QDL5cDO0czW}
```


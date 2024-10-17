#

## 1.Changing File Ownership:


```bash
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 root root 58 Oct 17 12:26 /flag
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 hacker root 58 Oct 17 12:26 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{M63_R4ySxTNbIjzHI1MWLfRAPOb.dFTM2QDL5cDO0czW}
```


## 2.Groups And Files:

```bash
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root root 58 Oct 17 12:32 /flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{8-A0P0yNzl9MSGq8AC0Dw2PwpG9.dFzNyUDL5cDO0czW}
```

## 3.Fun With Groups Names:

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp2011) groups=1000(grp2011)
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root root 58 Oct 17 12:38 /flag
hacker@permissions~fun-with-groups-names:~$ chgrp grp2011 /flag
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root grp2011 58 Oct 17 12:38 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{0jHWRgIee2KGXjDkslLIBvLq6Vx.dJzNyUDL5cDO0czW}
```

## 4.Changing Permissions:
```bash
r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - nothing
```
Eg.
```bash
r: the user that owns the file (user hacker) can read it
w: the user that owns the file (user hacker) can write to it
-: the user that owns the file (user hacker) cannot execute it
r: users in the group that owns the file (group hacker) can read it
-: users in the group that owns the file (group hacker) cannot write to it
-: users in the group that owns the file (group hacker) cannot execute it
r: all other users can read it
-: all other users cannot write to it
-: all other users cannot execute it
```


```bash
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 58 Oct 17 12:54 /flag
hacker@permissions~changing-permissions:~$ chmod a+rwx /file
chmod: cannot access '/file': No such file or directory
hacker@permissions~changing-permissions:~$ chmod a+rwx /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{wNN8V6IoLkkciBUYb_LLEqe2oQa.dNzNyUDL5cDO0czW}
```

## 5.Executable Files:


```bash

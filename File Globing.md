# File Globbing

## Matching with *

The * opertator fills in the remaining part with any number of characters (except . and /) that makes it match existing files 

To move to challenge with a max of 4 characters we
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{EFV2_mxjKcRVCVkrOmQrG-WDUbL.dFjM4QDL5cDO0czW}
```

## Matching with ?

The ? opertator fills in the remaining part with 1 character (except . and /) that makes it match existing files

To write the code to move to challenge without using c,l,*
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{A2HQ3J5DZ51OwHdjoQIUcsdxIBr.dJjM4QDL5cDO0czW}
```

## Matching with []
The [] opertator fills in the remaining part with the list of characters specified

To run the command with various files (file_b,file_a,file_s,file_h) we
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{8KTPrXROTL_3k39uBDjRcOui0_v.dNjM4QDL5cDO0czW}
```

## Matching Paths with []
This time instead of moving to /challenge/files we just use the absolute paths
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{MeRx4n7RoNkS5VUz8xQf9tur9w1.dRjM4QDL5cDO0czW}
```

## Mixing Globs 
This time we got a challenge where using max 6 character we need to match with the files challenging, educational, and pwning
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing      fantastic   kind        pwning     uplifting   zesty
beautiful    great       laughing    queenly    victorious
challenging  happy       magical     radiant    wonderful
delightful   incredible  nice        splendid   xenial
educational  jovial      optimistic  thrilling  youthful

hacker@globbing~mixing-globs:/challenge/files$ echo [cep]*
challenging educational pwning
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{sMqXY75xTQDtnrNGUC-Jf-Uzz1O.dVjM4QDL5cDO0czW}
```
To check all the files present we can use ls

To make sure the glob was right I used echo

## Exclusionary Globing

If ! is added at the start of [] it excludes all the contents from the glob

To run all the files that don't start with p, w, or n
```bash
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{wGhUycAl34kWCcP7hfKXB7DBcRh.dZjM4QDL5cDO0czW}
```

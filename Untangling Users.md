#


## 1.Becoming Users With su:


```bash
hacker@users~becoming-root-with-su:~$ su
Password:{hack-the-planet}
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{QpzSK32fPqQsXr_Pg0-S1grgg26.dVTN0UDL5cDO0czW}
```


## 2.Other Users With su


```bash
hacker@users~other-users-with-su:~$ su zardus
Password:{dont-hack-me}
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{oHDyZV26xe2ZBXjrkYV0ZQXSilr.dZTN0UDL5cDO0czW}
```

## 3.Cracking Passwords:


```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04803g/s 279.6p/s 279.6c/s 279.6C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:{aardvark}
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{IHtDOqhQ5Yl7ACRS2ZhLxl6H2GD.ddTN0UDL5cDO0czW}
```

## 4.Using sudo:


```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{cWFxh1-CUROg6EfbD8mOmOiC8ky.dhTN0UDL5cDO0czW}
```

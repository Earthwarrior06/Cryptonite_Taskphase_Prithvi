# Untangling Users


## 1.Becoming Users With su:

In this challenge, the su command is used to switch from the current user (hacker) to the root user. After providing the correct password, you gain elevated privileges, allowing you to read the /flag file that is only accessible by the root user.

The su command allows you to switch user identities, granting access to files and resources of that user, in this case, the root.

```bash
hacker@users~becoming-root-with-su:~$ su
Password:{hack-the-planet}
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{QpzSK32fPqQsXr_Pg0-S1grgg26.dVTN0UDL5cDO0czW}
```


## 2.Other Users With su

Here, you use su to switch to another user, Zardus. By entering Zardus's password, you can execute commands as that user and retrieve the flag by running the challenge program under Zardus’s account.

The su command can switch to any user account (not just root) if you know their password.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:{dont-hack-me}
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{oHDyZV26xe2ZBXjrkYV0ZQXSilr.dZTN0UDL5cDO0czW}
```

## 3.Cracking Passwords:

In this task, the password-cracking tool john is used to crack a password hash found in a file (e.g., /challenge/shadow-leak). Once the password is recovered, you switch to the cracked account and execute the challenge program to retrieve the flag.

john is a popular tool for cracking password hashes. Once the password is cracked, you can switch to the relevant user using su.

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

Here, the sudo command is used to execute a command with root privileges without needing to switch users. By using sudo, you can access files and perform tasks that require administrative privileges, such as reading the /flag file.

```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{cWFxh1-CUROg6EfbD8mOmOiC8ky.dhTN0UDL5cDO0czW}
```

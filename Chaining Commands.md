# Chaining Commands

## 1.Chaining with Semicolons:

";" separates commands in a similar way to how Enter separates lines (like C)
```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{MOwzyrqCBzS8RDO0Elxq6p3CtoA.dVTN4QDL5cDO0czW}
```


## 2.Your First Shell Script:

Used nano to open the shell to write the commands into it

We use bash to run scripts

```bash
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{8xXPWtC-acIIc8QkiGBSQnHi5uP.dFzN4QDL5cDO0czW}
```



## 3.Redirecting Script Output:

Using "|" we are able to pipe the output of a programme into a command
x.sh
```bash
/challenge/pwn;/challenge/college
```
```bash
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh|/challenge/solve
Correct! Here is your flag:
pwn.college{4BKuYpXfZLPWFuVSCDfS5DLe4De.dhTM5QDL5cDO0czW}
```

## 4.Executable Shell Scripts:

x.sh
```bash
/challenge/solve
```
Here we execute the script similar to how we execute commands (by calling them using relative or absolute paths)
```bash
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
-rw-r--r-- 1 hacker hacker 36 Oct 19 12:40 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod a+rwx x.sh
hacker@chaining~executable-shell-scripts:~$ nano x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{ovUOVLo5R4BCvpUrVD4YrX29oaI.dRzNyUDL5cDO0czW}
```

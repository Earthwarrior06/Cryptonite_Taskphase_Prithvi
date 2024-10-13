# Pondering Paths

## 1. The Root:
In this challenge, you execute /pwn from the root directory (/).

The flag appears after executing the command directly from the root.
```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{QTYVNnQqVYD1CFXm8WwvjC4vseT.dhzN5QDL5cDO0czW}
```
## 2. Program and Absolute Paths:
When you run /challenge/run, it works because you're providing an absolute path to the program.

Absolute paths start from the root directory (/), making them unambiguous.
```bash
Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{kbnEflpgcNMKzizDJ07N97o4Cd_.dVDN1QDL5cDO0czW}
```
## 3. Position Thyself:
Here, you navigate to /etc using cd /etc, and then run the command /challenge/run.

Even though you're in a different directory (/etc), the absolute path /challenge/run ensures the correct execution.
```bash
hacker@paths~position-thy-self:~$ cd /etc
hacker@paths~position-thy-self:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Y4dxlMveWzfL_YetYJYQHIgjfGi.dZDN1QDL5cDO0czW}
```
## 4. Position Elsewhere:
In this challenge, you navigate to the /etc directory using cd /etc and then run the command /challenge/run.

Since /challenge/run is an absolute path, it executes correctly, regardless of the fact that you're in the /etc directory.
```bash
Connected!
hacker@paths~position-elsewhere:~$ cd /etc
hacker@paths~position-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EtfAN45Dx5_kDq9JgN3ytxoZ0dP.ddDN1QDL5cDO0czW}
```
## 5. Position Yet Elsewhere:
In this challenge, you navigate to the /var/log directory using cd /var/log, and then run the command /challenge/run.

Since /challenge/run is an absolute path, it doesn’t depend on your current directory, allowing the command to execute correctly from anywhere in the filesystem.
```bash
hacker@paths~position-yet-elsewhere:/etc$ cd /var/log
hacker@paths~position-yet-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8IDHXXrkz8sqPljWQ0E7WYNrIHM.dhDN1QDL5cDO0czW}
```
## 6. Implicit Relative Paths from /:
Running challenge/run from the root directory shows an example of an implicit relative path.

Since you are in the correct directory (/), this works even without the ./ prefix.
```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gPv4aShYuDRkVVIG_VHWHJS-3-_.dlDN1QDL5cDO0czW}
```
## 7. Explicit Relative Paths:
Using ./challenge/run from the root directory explicitly states that you are using a relative path starting from the current directory (./).

```bash
hacker@paths~explicit-relative-paths-from-:/challenge$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{c52svT0Q9N_AkDn3nlOAZ7AEjae.dBTN1QDL5cDO0czW}
```
## 8.Implicit Relative Path
In this challenge, you navigate to the /challenge directory using cd /challenge and run the command ./run.

Since you are already in the correct directory (/challenge), using a relative path (./run) works perfectly.
```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YoiptIZOTmv_ia6VpPrvV5eUQs7.dFTN1QDL5cDO0czW}
```
## 9. Home Sweet Home:
Here, you create a file named a in your home directory and access it using the tilde (~), which is a shorthand for your home directory.

The file is written to and read back from /home/hacker/a.
```bash
hacker@paths~home-sweet-home:~$ touch a
hacker@paths~home-sweet-home:~$ /challenge/run /a
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{cLcinEs2x6vvjyF1VVkDsghmpod.dNzM4QDL5cDO0czW}
```

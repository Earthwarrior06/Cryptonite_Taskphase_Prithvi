### Pondering Paths

hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{QTYVNnQqVYD1CFXm8WwvjC4vseT.dhzN5QDL5cDO0czW}

Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{kbnEflpgcNMKzizDJ07N97o4Cd_.dVDN1QDL5cDO0czW}

hacker@paths~position-thy-self:~$ cd /etc
hacker@paths~position-thy-self:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Y4dxlMveWzfL_YetYJYQHIgjfGi.dZDN1QDL5cDO0czW}

Connected!
hacker@paths~position-elsewhere:~$ cd /etc
hacker@paths~position-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EtfAN45Dx5_kDq9JgN3ytxoZ0dP.ddDN1QDL5cDO0czW}

hacker@paths~position-yet-elsewhere:/etc$ cd /var/log
hacker@paths~position-yet-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8IDHXXrkz8sqPljWQ0E7WYNrIHM.dhDN1QDL5cDO0czW}

hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gPv4aShYuDRkVVIG_VHWHJS-3-_.dlDN1QDL5cDO0czW}

hacker@paths~explicit-relative-paths-from-:/challenge$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{c52svT0Q9N_AkDn3nlOAZ7AEjae.dBTN1QDL5cDO0czW}

hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YoiptIZOTmv_ia6VpPrvV5eUQs7.dFTN1QDL5cDO0czW}

hacker@paths~home-sweet-home:~$ touch a
hacker@paths~home-sweet-home:~$ /challenge/run /a
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{cLcinEs2x6vvjyF1VVkDsghmpod.dNzM4QDL5cDO0czW}

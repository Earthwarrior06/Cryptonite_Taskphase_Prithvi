# Digesting Documentation

## Learning From Documentation

For this programme we need to run the command /challenge/challenge with the arguement --give flag
```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{kK_DTq1RGEFd45SJmPaUKBYcaBK.dRjM5QDL5cDO0czW}
```

## Learning Complex Usage

For this programme we use the arguement --printfile _arguement_
The argument to the --printfile argument is the path of the flag to read

```bash
hacker@man~learning-complex-usage:/challenge$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{kS1JXD0D6nHfYttOMrMHnNhY9pb.dVjM5QDL5cDO0czW}
```

## Reading Manuals

man is short for manual, and will display (if available) the manual of the command we pass as an argument

```bash
hacker@man~reading-manuals:~$ man challenge
```
This will give us the manual for challenge
```bash
CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --ktqdhv NUM
              print the flag if NUM is 610

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
--More--
```
By pressing q to exit we then use the --ktqdhv NUM arguement
```bash
hacker@man~reading-manuals:/challenge$ /challenge/challenge --ktqdhv 610
Correct usage! Your flag: pwn.college{I6XJkRtMJC1q0TMV84VdLh3YvKr.dRTM4QDL5cDO0czW}
```

## Searching Manuals

Once again open challenge manual and search for the flag by typing
```bash 
hacker@man~searching-manuals:~$ man challenge
/flag
```
It will then show us 
```bash
--ib   A neat argument, but not the right one.

--oic  A neat argument, but not the right one.

--emzem
        This argument will give you the flag!

--eslgp
        A neat argument, but not the right one.
```
And more before and after
We now use --emzem as the arguement to /challenge/challenge
```bash
hacker@man~searching-manuals:~$ /challenge/challenge --emzem
Initializing...
Correct usage! Your flag: pwn.college{AKM4RXC6puuqdf9f9D9fZrEaGD1.dVTM4QDL5cDO0czW}
```

## Searching For Manuals

We first open the manual of the manual using
```bash
hacker@man~searching-for-manuals:~$ man man
```
From that we find out that we can use -k _dataSearchingForInManuals_ arguement on man
```bash
hacker@man~searching-for-manuals:~$ man -k challenge
lbviyvnlvv (1)       - print the flag!
```
We then search the manual lbviynlvv and follow the instructions given
```bash
hacker@man~searching-for-manuals:~$ man lbviyvnlvv

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --lbviyv NUM
              print the flag if NUM is 734

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
hacker@man~searching-for-manuals:~$ /challenge/challenge --lbviyv 734
Correct usage! Your flag: pwn.college{Qlb7JVUYSvi3UJLyvnKlvvabZhn.dZTM4QDL5cDO0czW}



hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 993
hacker@man~helpful-programs:~$ /challenge/challenge -g 993
Correct usage! Your flag: pwn.college{IJc9TE93ejpTN2RrMo61jSCkpLT.ddjM4QDL5cDO0czW}
```

## Helpful Programmes

Some programs don't have a man page, but might tell us how to run them if invoked with a special argument --help
To figure out what to do with challenge we use help
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AV9v-Mee".
```
We follow these instructions to get the flag
```bash
hacker@man~help-for-builtins:~$ challenge --secret AV9v-Mee
Correct! Here is your flag!
pwn.college{AV9v-MeewGSyBaQUfux2wSty1YZ.dRTM5QDL5cDO0czW}
```

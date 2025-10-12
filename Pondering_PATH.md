# Linux Luminarium: PATH

## The PATH Variable
This challenge includes `PATH` shell environment variable, which is a colon-separated list of directories where the shell searches for executable programs when a bare command name is entered.

### Solve
**Flag:** pwn.college{cdNU81bUdfZNR_frYHG7LwSUNPV.QX2cDM1wyM3AzNzEzW}

```
hacker@path~the-path-variable:~$ echo $PATH
/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{cdNU81bUdfZNR_frYHG7LwSUNPV.QX2cDM1wyM3AzNzEzW}
```


### New Learnings
I learnt how the compiler fetches commands as child processes and how it can be manipulated by path variable. 

### References 
referred to given text

---

## 2. Setting PATH
This challenge demonstrates how to **explicitly set the `PATH` variable** to include a non-standard directory containing a custom command. By assigning the `PATH` to a directory containing a necessary executable (e.g., `win`), the shell can find and execute that command using its bare name. This illustrates how administrators and users can customize their execution environment to use personal or locally installed tools.

### Solve
**Flag:** pwn.college{ctSvZ0_mXVTSY2cQgtYakm3CY1O.QX1cjM1wyM3AzNzEzW}

```
hacker@path~setting-path:~$ PATH="/challenge/more_commands/"
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{ctSvZ0_mXVTSY2cQgtYakm3CY1O.QX1cjM1wyM3AzNzEzW}
```

### New Learnings
I learnt that you can manually the value in PATH! and thus make us capable of exceuting any program as a command without defining its path.

### References 
referred to given text

---

## 3. Finding Commands
This section introduces the **`which` command**, a utility that mirrors the shell's behavior by searching the directories listed in the `$PATH` variable in order. `which` reports the **absolute path** of the first executable file it finds that matches the given command name. This is an essential skill for quickly locating the exact program being executed.

### Solve
**Flag:** pwn.college{MRFNw2nAQgFId6OiEQ4BEYexNuh.01NzEzNxwyM3AzNzEzW}

I found the path of win using which and ls'd through that directory and cat'd the flag file. 
```
hacker@path~finding-commands:~$ which win
/challenge/paths/3826/win
hacker@path~finding-commands:~$ ls /challenge/paths/3826/win
/challenge/paths/3826/win
hacker@path~finding-commands:~$ ls /challenge/paths/3826
flag  win
hacker@path~finding-commands:~$ cat /challenge/paths/3826/flag
pwn.college{MRFNw2nAQgFId6OiEQ4BEYexNuh.01NzEzNxwyM3AzNzEzW}
```

### New Learnings
You can use which to find the exact location of a command (which will fetch it from path env variable)

### References 
referred to given text

---

## 4. Adding Commands
This challenge focuses on **extending the `PATH` variable** to include a new directory *without* overwriting existing system paths. This is typically done by prepending or appending the new directory to the existing `$PATH` using shell variable expansion (e.g., `PATH=/my/new/dir:$PATH`). The concept highlights how to permanently integrate custom tools into the execution environment while maintaining access to all standard utilities.

### Solve
**Flag:** pwn.college{ARqI08xigw5XCY7d6s16IwxdnNB.QX2cjM1wyM3AzNzEzW}

```
hacker@path~adding-commands:~$ ls -l | grep win
-rwxr-xr-x 1 hacker hacker  22 Oct 12 07:17 win
hacker@path~adding-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ PATH="/run/dojo/bin/cat:/home/hacker"
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/home/hacker/win: line 2: cat: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~adding-commands:~$ PATH="/run/dojo/bin:/home/hacker"
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{ARqI08xigw5XCY7d6s16IwxdnNB.QX2cjM1wyM3AzNzEzW}
```


### New Learnings
revised all concepts. 

### References 
referred to given text

---

## Hijacking Commands


### Solve
**Flag:** NOT OBTAINED


### New Learnings
Brief note on what ou learned from the challenge

### References 
referred to given text








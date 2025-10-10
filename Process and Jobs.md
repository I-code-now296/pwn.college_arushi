# Linux Luminarium: Processes

## Listing Processes
First, we will learn to list running processes using the ps command and -ef / aux .

### Solve
**Flag:** pwn.college{gkcfsFzipv4t7hGmBN65L4kTCgl.QX4MDO0wyM3AzNzEzW}

I checked the running processes using `pw aux` command. I saw one with the word challenge in and I ran that. It worked!

### New Learnings
I learnt whaat processes are. I learnt how to check all running processes. I learnt the use of -e, -f, and aux
standered: -e to list "every" process and -f for a "full format"
BSD syntax: a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output. These
### References 
refered text given. 

---

## Killing Processes
After having launched processes, viewed processes, this is to terminate processes using kill command.

### Solve
**Flag:** pwn.college{I-ELZN5vmwf4hmYjcBQExQaZOqv.QXyQDO0wyM3AzNzEzW}

```
bash
hacker@processes~killing-processes:~$ ps -ef | grep dont_run
hacker       136     135  0 11:05 ?        00:00:00 /challenge/dont_run
hacker       168     152  0 11:09 pts/0    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{I-ELZN5vmwf4hmYjcBQExQaZOqv.QXyQDO0wyM3AzNzEzW}
```

### New Learnings
Kill is used to terminate it by passing the process identifier (the PID from ps) as an argument.
syntax: kill <pid>


### References 
NA

---

## Interrupting Processes
Introduces concept of process termination in Linux terminals using the Ctrl-C hotkey. This causes the application to cleanly exit


### Solve
**Flag:** pwn.college{Ac_aJtVLONPdoA4JJD65Uvbi6wr.QXzQDO0wyM3AzNzEzW}

```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{Ac_aJtVLONPdoA4JJD65Uvbi6wr.QXzQDO0wyM3AzNzEzW}
hacker@processes~interrupting-processes:~$ 
```


### New Learnings
process can sometimes get clogged. we can use the hotkey ctrl + c to pause this. 


### References 
the text given.

---

## Killing Misbehaving Processes
In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo.

### Solve
**Flag:** pwn.college{0TiwPCK9ATwT8GGqv2vDSIsPIgd.0FNzMDOxwyM3AzNzEzW}

I first checked all orcessSo, I tried excecuting /challenge/run. It got stuck; so I did ctrl+c and I checked the ps aux again. There was another decoy file so I tried to kill that. It worked. But now when I read the file I had many many decoy flags. So I ran `/challenge/run` again and cat'd the file. Got the flag. 



### New Learnings
Practices the concepts of veiwing, obtaining PID, killing and pausing processeses.

### References 
Referred given text.

---

## Suspending Processes
Suspeninding processes can be done through the ctrl + z command. It will suspend a process, not kill it.
This level's run wants to see another copy of itself running and using the same terminal.

### Solve
**Flag:** pwn.college{MFw6gMi5bxlQVuXzlWLR43zD2QM.QX1QDO0wyM3AzNzEzW}

### New Learnings
Suspeninding processes can be done through the ctrl + z command. It will suspend a process, not kill it.

### References 
Given text. 

---

## Resuming Processes
This challenge's run needs you to suspend it, then resume it using a fg commands (which will push a suspended command into the foreground.)

### Solve
**Flag:** pwn.college{8Cg_27ft8yvI74g0YB5CQTtq_P1.QX2QDO0wyM3AzNzEzW}

called `/challenge/run`, suspended it using ctrl+z and ran it again using fg. 


### New Learnings
you can resume a suspended process with the fg command (bring it to the fore ground).

### References 
refer given text.

---

## Backgrounding Processes
Covers bg.
fg command resumes a job in the foreground, granting it control of the terminal, while the bg command resumes a job in the background, allowing it to execute while immediately returning the shell's command prompt to the user.

### Solve
**Flag:** pwn.college{Uac2rM0s6YfVG_BiAWOsPOpEJOw.QX3QDO0wyM3AzNzEzW}

Ran `/challenge/run`, suspend it with ctrl + z, resume it in the background with bg and run another /challenge/run. 


### New Learnings
Difference between background processes, foreground processes (with a +) how to use bg on a suspended process.

### References 
Given file referenced. 

---

## Foregrounding Processes
You can foreground a backgrounded process with fg just like you foreground a suspended process. Just use fg command again. 

### Solve
**Flag:** pwn.college{ARo_WI2bWXbVvF0A-qze2T6kTaO.QX4QDO0wyM3AzNzEzW}

Ran `/challenge/run`, suspend it with ctrl + z, resume it in the background with `bg` and bought it to the foreground with `fg`.  

### New Learnings
you can bring any file to the foreground using fg. 

### References 
Given text.

---

## Starting Backgrounded Processes
You can use `<process> &` (Appended with a &) to directly start a file in the background. 

### Solve
**Flag:** pwn.college{YTvWb09w48MaKdmQsxwK29TmlUx.QX5QDO0wyM3AzNzEzW}

'''
bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 147
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{YTvWb09w48MaKdmQsxwK29TmlUx.QX5QDO0wyM3AzNzEzW}
'''

### New Learnings
I learnt how to run processes in the background directly. 

### References 
Given text.

---

## Process Exit Codes
You must retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument.

### Solve
**Flag:** pwn.college{kx56WR9St_34iux18RSGAQzyvc2.QX5YDO1wyM3AzNzEzW}
```
hacker@processes~process-exit-codes:~$ echo /challenge/get-code $?
/challenge/get-code 130
hacker@processes~process-exit-codes:~$ /challenge/submit-code 130
Incorrect... Make sure to use $? immediately after running /challenge/get-code. 
Your shell will overwrite the $? variable with the exit value of any other 
command you run!
hacker@processes~process-exit-codes:~$ /challenge/get-code $?
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
14
hacker@processes~process-exit-codes:~$ /challenge/submit-code 14
CORRECT! Here is your flag:
pwn.college{kx56WR9St_34iux18RSGAQzyvc2.QX5YDO1wyM3AzNzEzW}
```

### New Learnings
I learnt about exit code for every program and every builtin, that can be accessed by both shell or user.

### References 
Text given








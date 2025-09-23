# PONDERING PATHS

## The Root
To understand what the root directory is and how to access it. 

### Solve
**Flag:** `pwn.college{MRVNhvNden4d73KCCAXAXzvZJvM.QX4cTO0wyM3AzNzEzW}`

### I typed the command /pwn as instructed to acces this program from the root (i.e. /). This would be the absolute path for pwn 

```bash
/pwn
```

### New Learnings: I learnt what a directory is, what a root is, and how to acess a file using its absolute path. 

### References : NA


## 2. Programs and absolute paths
To access files using its absolute path

### Solve
**Flag:** `pwn.college{ozIxHWsAgILwUiQzRheR3C-zu6p.QX1QTN0wyM3AzNzEzW}`

### I typed the command /challenge/run as instructed to access this program from the root (i.e. /). This would be the absolute path for run 

```bash
/challenge/run
```

### New Learnings: I learnt the use of / in accessing files inside the directory for absolute path. 

### References : NA

## 3. Position Thyself
To change directory using cd command

### Solve
**Flag:** `pwn.college{0kvpiQqWsFg_-GcTTtGw7ICkR9A.QX2QTN0wyM3AzNzEzW}`

### I typed the command /challenge/run. It asked me to change the directory which I did. And then I retyped the command. 


### New Learnings: I learnt the use of cd. 

### References : NA


## 4. Position elsewhere
To change directory using cd command

### Solve
**Flag:** ` pwn.college{YwbLkOxVOjd05TEZ4O4l54v5DQI.QX3QTN0wyM3AzNzEzW}`

### I typed the command /challenge/run. It asked me to change the directory which I did. And then I retyped the command. 


### New Learnings: I learnt the use of cd. 

### References : NA


## 5. Position yet elsewhere
To change directory using cd command

### Solve
**Flag:** `pwn.college{08yGFQ0v3gahblS-BYP5M-A0tkX.QX4QTN0wyM3AzNzEzW}`

### I typed the command /challenge/run. It asked me to change the directory which I did. And then I retyped the command. 


### New Learnings: I learnt the use of cd. 

### References : NA


## 6. Implicit relstive paths, from/
To understand relative paths.

### Solve
**Flag:** `pwn.college{wrz5eQ1il5sMpgyhG7zIbQhCmEm.QX5QTN0wyM3AzNzEzW}`

### I first changed the directory to / (root). From there aI directly accessed run typing challenge/run

```bash
cd /
challenge/run
```
 


### New Learnings: I learnt how to access files through implicit relative path 

### References : NA


## 7. explicit relstive paths, from/
To understand relative paths and the use of '.' (to indicate in the same directory)

### Solve
**Flag:** `pwn.college{UmfKrwf05coRTqV4rSHmec-spD8.QXwUTN0wyM3AzNzEzW}`

### I first changed the directory to /. From there I directly accessed run typing .challenge/run

```bash
cd /
.challenge/run
```

### New Learnings: I learnt how to access files through explicit relative path using a full stop.

### References : NA



## 8. implicit relstive path
To understand relative paths and the use of '.' (to indicate in the same directory) in more depth

### Solve
**Flag:** `pwn.college{ItfLlGSEXAPdhXDYq3vaVLVqJ_H.QXxUTN0wyM3AzNzEzW}`

### I first changed the directory to /challenge. From there I directly accessed run typing ./run

```bash
cd /challenge
./run
```

### New Learnings: I learnt how to access files through explicit relative path using a full stop.

### References : NA


## 9. Home sweet home 
understand home directory and how it is expressed as ~. To access home/hacker through ~

### Solve
**Flag:** ` pwn.college{geRKe6GdRpcsa4qdJ_7qPMo4y5G.QXzMDO0wyM3AzNzEzW}`

### I excecuted thre command /challenge/run ~/a  .To make is less than three characters I used the shortcut for /home/hackers, ie ~
```bash
cd /
/challenge/run ~/a
```
 


### New Learnings: I learnt what a home directory is and what is the use of it.

### References : NA






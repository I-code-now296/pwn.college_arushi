# Comprehending Commands

## 1. cat: not the pet but the command!
 
understand how to read and concatenate files using command cat

### Solve
**Flag:** ` pwn.college{sAHhS2Q753S45caWIYTsD4G2P6P.QXxcTN0wyM3AzNzEzW}`

###I went to the home directory and used the cat command to access the flag file ~
```bash
cd /
cat flag
```
 


### New Learnings: I learnt what a cat command is and what is the use of it.

### References : NA



## 2. catting absolute paths
 
understand how to read files through their absolute paths using cat

### Solve
**Flag:** ` pwn.college{Qv9DWfwI1ol9_Le2LkEMDgWcwK1.QX5ETO0wyM3AzNzEzW}`

###I typed in the command ~
```bash
cat /flag
```
 


### New Learnings: I learnt what a cat command is and what is the use of it.

### References : NA





## 3. more catting practice
 
understand how to read absolute path of files using command cat

### Solve
**Flag:** `pwn.college{4sOi_3QK0dyvathQyxg4qEiQUNk.QXwITO0wyM3AzNzEzW}`

###I I used the cat command to access access the flag file by typing in the exact file directory given by them ~
```bash
cat file /lib/llvm-10/include/flag
```
 


### New Learnings: I learnt what a cat command is and what is the use of it.

### References : NA




## 4. grepping for a needle in the haystack
 
Learning how to use grep in place of cat. grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

### Solve
**Flag:** ` pwn.college{0adgti4r_YuwCwj7o3Ek_BA6I2y.QX3EDO0wyM3AzNzEzW}`

###I typed in the command grep. I replaced SEARCH_STRING with string in the flag: pwn.college. I searched in the file absolute path sirectory~
```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
```
 


### New Learnings: I learnt what a grep command is and what is the use of it.

### References : NA


## 5. Comparing files 

Learning how to use diff. diff compares two files line by line and shows you exactly what's different between them.

### Solve
**Flag:** ` pwn.college{82K0q__32wKmQYkE_qzj9O-Z94O.01MwMDOxwyM3AzNzEzW}`

###I went to the challenge directory using cd. I compared thr teo files using diff~
```bash
hacker@commands~comparing-files:~$ cd /challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt
86a87
```
 
### New Learnings: I learnt what a diff command is and what is the use of it.

### References : NA







# 1. Printing Variables
Challenge asks me to print `FLAG` variable

## My solve
**Flag:** `pwn.college{k2z7cCgLTDFn1KSg3RU478IqiVO.QX3UTN0wyM3AzNzEzW}`

- First I connected my terminal to dojo using SSH
- Then I typed `echo $FLAG`
- This gave me the flag

## What I learned
- I learnt how to get output from a shell variable

## References 
Referred text given in challenge

---

# 2. Setting Variables
I am asked to set variable `PWN` with value `COLLEGE`

## My solve
**Flag:** `pwn.college{s5pNd7UNjSFzyXNjISVIpXPXVid.QX5UTN0wyM3AzNzEzW}`

- Entering `PWN=COLLEGE` gives the flag

## What I learned
- I learnt how to set value to a variable

## References 
Referred text given in challenge

---

# 3. Multi-word Variables
Set a multiword variable value

## My solve
**Flag:** `pwn.college{8WQXN1MBWNg0wVflTYxJeKKUvCG.QXwYTN0wyM3AzNzEzW}`

- I typed `PWN="COLLEGE YEAH"`
- The quotations are so that it takes it as one string instead of two seperate inputs

## What I learned
- I learnt how to setup multi word value to a variable

## References 
Referred text given in challenge

---

# 4. Exporting Variables
I was asked to create 2 varibles and assign them values, but only export one variable

## My solve
**Flag:** `pwn.college{YyzjBq4VvuCh8rlwyXrDbMhz9b_.QXyYTN0wyM3AzNzEzW}`

- First I typed `PWN=COLLEGE`
- Then I exported using `export PWN`
- Then I created `COLLEGE=PWN` and didn't export it
- Then I ran `/challenge/run` to get the flag

## What I learned
- I learnt how to export a flag

## References 
Referred text given in challenge

---

# 5. Printing Exported Variables
I was asked to use `env` command which shows all the exported variables

## My solve
**Flag:** `pwn.college{seEQ7i7nnJYiL3P7mXLB6q7weCx.QX4UTN0wyM3AzNzEzW}`

- Using `env` , I got output:
going though the output I picked out the one that would give me the flag. 

## What I learned
- I learnt about `env` command which shows all exported varibles and their values

## References 
Referred text given in challenge

---

# 6. Storing Command Output
I was asked to store output of a command in a varible then print that variable

## My solve
**Flag:** `6. pwn.college{UuZ7yXDW7wDnnEKvaH6FYdPQKR9.QX1cDN1wyM3AzNzEzW}`

`PWN=$(/challenge/run)`
Then I read PWN to get the flag. 

## What I learned
- I learnt how to copy output of a command in a variable

## References 
Referred text given in challenge

---

# 7. Reading Input
I am asked to use `read` to get input inside a variable

## My solve
**Flag:** `pwn.college{kc5i4ao5abat9Qo4_ysU_oW27Ln.QX4cTN0wyM3AzNzEzW}`

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
```

## What I learned
- I learnt how to use `read` command to get input for a variable

## References 
Referred text given in challenge

---

#8. Reading Files
I was asked to input a file inside variable

## My solve
**Flag:** `pwn.college{gN6Z8yPoalYpC3_bEDO_fN8K469.QXwIDO0wyM3AzNzEzW}`

- I wrote `read PWN < /challenge/read_me`
- This added input inside variable

## What I learned
- I learnt how to directly input a file inside a variable

## References 
Referred text given in challenge

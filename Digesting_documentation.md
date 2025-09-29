# Learning From Documentation
The challange asks me to read a basic documentation provided in challenge and use flags with command based on that.

## My solve
**Flag:** `pwn.college{ccf2nnZGqlKL29iLYaT0A2wmD1_.QX0ITO0wyM3AzNzEzW}`

I was asked to use flag `--giveflag` with absolute path `/challenge/challenge`
So I invoked this using `/challenge/challenge --giveflag`

## What I learned
- I learnt how to understand basic documentation and use flags with commands
  
## References 
Referred text given in challenge on pwn.college

---

# Learning Complex Usage
Challenge gives me an example and brief documentation on how I can use `--printfile` argument with `/challenge/challenge` to printout a file. So I am asked to find flag using this.

## My solve
**Flag:** `pwn.college{0BvVZEdt9DlfNgK76mlp4rY6h6J.QX1ITO0wyM3AzNzEzW}`

I first tried various iteration with different arguments for printfile like  `/challenge/challenge --printfile /challenge/challenge` or `/challenge/challenge --printfile /challenge/file`
In one of my attempts I wrote `/challenge/challenge --printfile /flag`. This gave me the flag

## What I learned
- I learnt how to read more complex documentations, and thus use arguments with flags
- Also realised we did similar action with find command, which was a nice recap

## References 
Referred text given in description of challenge

---

# Reading Manuals
The challenge asks me to use man command to read documentation of challenge command

## My solve
**Flag:** `pwn.college{AcQknwNDW-aKrCLfYx2x3DhtC0u.QX0EDO0wyM3AzNzEzW}`

- I used `man challenge`
- This told me about `/challenge/challenge` command
- It also told me about `----cknwar` flag which returns flag when I use `230` as argument with it.

## What I learned
- I learnt about man command ~~(my fav command; only reason I am still alive after using fmmpeg lmao)~~
- I learnt how to properly read it and learn more about flags used with command through man pages

## References 
Referred description provided with the challenge

---

# Searching Manuals
Challenge asks me to man challenge command and thus find flag inside it

## My solve
**Flag:** `pwn.college{M4PRuuw72-fFLOEeaBaj1jooKvM.QX1EDO0wyM3AzNzEzW}`
- I used `man challenge`
- This told me I need to use `/challenge/challenge`
- I searched through man page with `/flag` to find the argument which gives flag
- Then I pressed `q` to go back
- Finally I wrote `/challenge/challenge --acvwa` to get the flag

## What I learned
- I learnt how to search in man pages
- I can even use `n` and `N` to check next search result
- `/` is used to search from top to bottom and `?` is used to search from bottom to top

## References 
- I referred text provided in challenge
- I also used basic linux command wiki to properly understand differencce between `/` and `?` when searching through man pages

---

# Searching For Manuals
The challenge asks me to man the man page and find hidden flag through which I can find changed man page of challenge and then find flag through it

## My solve
**Flag:** UNSOLVED


## What I learned
- I learnt how read man pages

## References 
- Referred description in challenge and read `man man`

---

# Helpful Programs
The challenge asked me to make use of `--help`

## My solve
**Flag:** `pwn.college{0BvVZEdt9DlfNgK76mlp4rY6h6J.QX1ITO0wyM3AzNzEzW}`

- Usually /challenge/challenge is used for flag
- So I used `/challenge/challenge -h`
- This gave me description for `-p` and `-g`
- I got the number specified number from `-p` and then entered it as argument with `-g`
- This gave me the flag

## What I learned
- I learnt how to use `--help` or `-h` when man page is not available

## References 
I referred description in challenge

---

# Help for Builtins
Challenge asks me to use help command with an argument to directly get usage of its flags

## My solve
**Flag:** `pwn.college{c6UTgw2wuhZWF-NZY5Eh7POUaCK.QX0ETO0wyM3AzNzEzW}`

 I used `help challenge`.  The output told me info about `--secret` flag and the value I need to input `c6UTgw2w`
Thus I typed:
```pwn.college{c6UTgw2wuhZWF-NZY5Eh7POUaCK.QX0ETO0wyM3AzNzEzW}```


## What I learned
- I learnt how to use help command directly to view info about flags

## References 
Referred text in challenge

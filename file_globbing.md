# Matching with *
Challenge asks me to cd into /challenge with only use of less than 4 characters in argument

## My solve
**Flag:** `pwn.college{8g2J7do6dvInyCKPKzfUU666-9Y.QXxIDO0wyM3AzNzEzW}`

- I wrote `cd /ch*`
- This is less than 4 characters
- Also it autocompletes `/ch*` to `/character`

## What I learned
- `*` is treated as wildcard, it autocompletes as per the context
- It matches any part of file name except `/` leading with `.`
- 
## References 
- Referred text in challenge
- Also looked a little bit of bash manual

---

# Matching with ?
Challenge asks me to switch c and l with ? when using cd to go into /challenge

## My solve
**Flag:** `pwn.college{MLhwB5KNas9qE-8b2roKI4eT_Vh.QXyIDO0wyM3AzNzEzW}`

- I typed `cd /?ha??enge`
- This replaced it with `cd /challenge` in terminal
- Then I ran `/challenge/run`
- This gave me the flag

## What I learned
- I learnt I can use `?` as a replacement for character while writing input in terminal
- This is similar to `*` but limited to one character

## References 
Referred text given in challenge

---

# Matching with []
I am asked to cd into `/challenge/file`
Then asked to run `/challenge/run` with argument where I can glob multiple files together

## My solve
**Flag:** `pwn.college{Qds5cb_pJo1fN0-1P3zZzpfd8cM.QXzIDO0wyM3AzNzEzW}`

- First I wrote `cd /challenge/file`
- Then I ran `/challenge/run file_[absh]`

## What I learned
- I learnt I can use `[]` to glob files
- It is similar to, `?` but limited to charadcters entered

## References 
Referred text given in challenge

---

# 4. Matching paths with []
I was asked to run `/challenge/run` with usage of `[]` in argument (while defining a path)

## My solve
**Flag:** `pwn.college{Ux6FpzSontn9uQ5VFlc1xh1Jw8D.QX0IDO0wyM3AzNzEzW}`

- I ran `/challenge/run /challenge/files/file_[bash]`
- This includes the given path in argument
- Also `[]` are used to glob multiple files 

## What I learned
- I learnt how to use `[]` in file paths

## References 
Referred text in given challenge

---

# 5. Multiple globs
I was asked to run `/challenge/run` followed by an argument that covers all the words with letter p in it

## My solve
**Flag:** `pwn.college{sz5y1fyWYzfbwYQG52_I0212T2g.QX1IDO0wyM3AzNzEzW}`

- I cd'd into `/challenge/files`
- Then I wrote `/challenge/run *p*`
- This covers every letter with in start,middle or end
- Thus I got the flag

## What I learned
- I learnt how to use globbing multiple times in a single argument

## References 
I just referred the text provided in challenge
---

# 6. Mixing globs
Challenge asks me to use multiple globbings to find files specified in challenge

## My solve
**Flag:** `pwn.college{gvx5MHEm8EKR7XkIRIqE3MSos1X.QX2IDO0wyM3AzNzEzW}`

- First I cd'd into `/challenge/files`
- Then I used `ls`, so I can get idea of other files and they don't conflict when I use globbing
- After that I decided to type `/challenge/run [cep]*`
- This means word starting from c,e and p. Followed by any characters. It didn't conflict with other files
- Thus I got the flag


## What I learned
- I learnt how to use multiple globbings together as a combo to find files we want

## References 
Referred text provided in challenge

---

# 7. Exclusionary globbing
The challenge asks me to cd into `/challenge/files`, then find files using globbing that don't start with `p`, `w` abd `n`

## My solve
**Flag:** `pwn.college{gvx5MHEm8EKR7XkIRIqE3MSos1X.QX2IDO0wyM3AzNzEzW}`

- I cd'd into `/challenge/files`
- Then I ran `/challenge/run [!pwn]*`
- The `!` specifies to exclude files starting from either `p`, `w` or `n`
- The `*` means any characterse after `p`, `w` and `n`

## What I learned
- I learnt how to exclude files with `!` or `^`
- Also recapped using multiple file globbing

## References 
Referred text provided in challenge

---

# 8. Tab completion
Challenge asks me to use tab to cat a file named similar to `challenge/pwncollege`

## My solve
**Flag:** `pwn.college{cwKusYxBTdgE5JO0FVrjfUNCtaL.0FN0EzNxwyM3AzNzEzW}`

- I wrote `/challenge/pw`
- Then I pressed TAB
- This auto completed it to `/challenge/pwncollege` (well it has some space at the end, but yeah)

## What I learned
- I learnt how to use TAB key to autocomplete file paths or commands ~~(please use fzf-tab)~~

## References 
Referred text in challenge

---

# 9. Multiple options for tab completion
The challenge asks me to use tab and figure out flag when there are multiple options

## My solve
**Flag:** `pwn.college{gwFLCfna6beCax5dy4wPobXvKF5.0lN0EzNxwyM3AzNzEzW}`

- At first I kept running path which didn't work for any file
- I tried all the files that came up with two tab presses but none of them included the flag.
- then i tried reading all those files using cat which still didn't work
- then I tried the cat command with `cat /challenge/files/p[tab]` which gave me /challenge/files/pwncollege-flag which I cat'd and got the flag.  

## What I learned
- I learnt multiple autocompletes can tab completion

## References 
I referred text given in challenge

---

# 10. Tab completion on commands
Challenge asks me to enter command `pwncollege` and press TAB to autocomplete it

## My solve
**Flag:** `pwn.college{oaUJ0K2bd1m85Ujbf4Lm3QD3j8c.0VN0EzNxwyM3AzNzEzW}`
- I wrote `pwncollege`
- Pressed TAB
- This auto completed it with `pwncollege-31086`
- Running this command gave me the flag

## What I learned
- I learnt I can even use TAB to autocomplete commands and it must be done cautiously.

## References 
Referred text given in challenge

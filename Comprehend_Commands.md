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


## 7. Touching files 

Learning how to create new files using the touch command.

### Solve
**Flag:** ` pwn.college{I3wpEaTRw0Q0ccy6y9MhANu4ILB.QXwMDO0wyM3AzNzEzW} `

###I created 2 files using touch command. ~
```bash
Connected!
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ ls
a
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{I3wpEaTRw0Q0ccy6y9MhANu4ILB.QXwMDO0wyM3AzNzEzW}
hacker@commands~touching-files:~$
```
 
### New Learnings: I learnt what a touch command is and what is the use of it.

### References : NA


## 8. Removing files 

Learning how to remove files using the rm command.

### Solve
**Flag:** ` pwn.college{A3AwQQo8F4fd6m7ukuGYqcSgdI4.QX2kDM1wyM3AzNzEzW} `

###I deleted delete_me file using rm command. ~
```bash
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ ls
a  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
a
hacker@commands~removing-files:~$ /challenge/run
bash: /challenge/run: No such file or directory
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{A3AwQQo8F4fd6m7ukuGYqcSgdI4.QX2kDM1wyM3AzNzEzW}
```
 
### New Learnings: I learnt what a remove rm command is and what is the use of it.

### References : NA


## 9. Hidden files 

Learning how to access hidden files (with .) using the ls -a command.

### Solve
**Flag:** ` pwn.college{UiE86xLTb9QnVHTdWWbY3xsPgjM.0VOxEzNxwyM3AzNzEzW}  `

###I created 2 files using touch command. ~
```bash
Connected!
hacker@commands~hidden-files:~$ ls -a
.  ..  .bash_history  .config  a
hacker@commands~hidden-files:~$ cat .config
cat: .config: Is a directory
hacker@commands~hidden-files:~$ cat .
cat: .: Is a directory
hacker@commands~hidden-files:~$ cat ..
cat: ..: Is a directory
hacker@commands~hidden-files:~$ cat .flag
cat: .flag: No such file or directory
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.                     bin        etc    lib64   nix   run   tmp
..                    boot       home   libx32  opt   sbin  usr
.dockerenv            challenge  lib    media   proc  srv   var
.flag-13336659621459  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ cat .flag-13336659621459
pwn.college{8EKFp8ua7cG2crA3txOZGqN2Hbw.QXwUDO0wyM3AzNzEzW}
```
 
### New Learnings: I learnt what a hidden file is and the command to access it.

### References : NA



## 10. An Epic Filesystem Quest 


### Solve
**Flag:** ` pwn.college{YCJJa1oL6AfzT9d6aJD7-YHG85E.QX5IDO0wyM3AzNzEzW} `

###TO find the hidden flag  cd, ls, and cat. ~
```bash
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat MEMO
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/riscv/net

Watch out! The next clue is *trapped*. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ ls /opt/linux/linux-5.4/arch/riscv/net
Makefile  TEASER-TRAPPED  bpf_jit_comp.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat /opt/linux/linux-5.4/arch/riscv/net/TEASER_TRAPPED
cat: /opt/linux/linux-5.4/arch/riscv/net/TEASER_TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ ls /opt/linux/linux-5.4/arch/riscv/net
Makefile  TEASER-TRAPPED  bpf_jit_comp.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat /opt/linux/linux-5.4/arch/riscv/net/TEASER_TRAPPED
cat: /opt/linux/linux-5.4/arch/riscv/net/TEASER_TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat TEARER_TRAPPED
cat: TEARER_TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat /opt/linux/linux-5.4/arch/riscv/net/TEACHER-TRAPPED
cat: /opt/linux/linux-5.4/arch/riscv/net/TEACHER-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cat /opt/linux/linux-5.4/arch/riscv/net/TEASER-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/locale

The next clue is *hidden* --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/xtensa/variants/csp/include/variant$ cd /usr/share/locale
hacker@commands~an-epic-filesystem-quest:/usr/share/locale$ ls
ab     chr        frp    ja.euc-jp  mo        pt_PT      tr
ace    ckb        fur    jam        mr        ro         tt
ach    crh        fy     ka         ms        ru         tt@iqtelif
af     cs         ga     kab        mt        rw         ug
ak     cs.cp1250  gez    ki         my        sc         uk
am     csb        gl     kk         na        sd         uk_UA
an     cv         gn     kl         nah       si         ur
ar     cy         gu     km         nb        sk         uz
as     da         gv     kn         nb_NO     sk.cp1250  ve
ast    de         ha     ko         ne        sl         vi
ay     dv         haw    ko.UTF-8   nl        so         wa
az     dz         he     kok        nn        son        wal
ba     ee         hi     ku         no        sq         wo
bar    el         hi_IN  kv         nso       sr         xh
be     en         hr     kw         nv        sr@latin   yo
bg     en_GB      ht     ky         oc        sv         zh
bi     eo         hu     lo         or        sw         zh_CN
bn     es         hy     lt         pa        ta         zh_CN.UTF-8
bn_IN  et         ia     lv         pap       te         zh_HK
br     eu         id     mai        pi        tg         zh_Hant
bs     fa         io     mhr        pl        th         zh_TW
byn    ff         is     mi         pl.UTF-8  ti         zh_TW.UTF-8
ca     fi         it     mk         ps        tig        zu
ce     fo         iu     ml         pt        tk
ch     fr         ja     mn         pt_BR     tl
hacker@commands~an-epic-filesystem-quest:/usr/share/locale$ ls -a
.      ce         fr     ja.euc-jp  mr        ru          ug
..     ch         frp    jam        ms        rw          uk
.TIP   chr        fur    ka         mt        sc          uk_UA
ab     ckb        fy     kab        my        sd          ur
ace    crh        ga     ki         na        si          uz
ach    cs         gez    kk         nah       sk          ve
af     cs.cp1250  gl     kl         nb        sk.cp1250   vi
ak     csb        gn     km         nb_NO     sl          wa
am     cv         gu     kn         ne        so          wal
an     cy         gv     ko         nl        son         wo
ar     da         ha     ko.UTF-8   nn        sq          xh
as     de         haw    kok        no        sr          yo
ast    dv         he     ku         nso       sr@latin    zh
ay     dz         hi     kv         nv        sv          zh_CN
az     ee         hi_IN  kw         oc        sw          zh_CN.UTF-8
ba     el         hr     ky         or        ta          zh_HK
bar    en         ht     lo         pa        te          zh_Hant
be     en_GB      hu     lt         pap       tg          zh_TW
bg     eo         hy     lv         pi        th          zh_TW.UTF-8
bi     es         ia     mai        pl        ti          zu
bn     et         id     mhr        pl.UTF-8  tig
bn_IN  eu         io     mi         ps        tk
br     fa         is     mk         pt        tl
bs     ff         it     ml         pt_BR     tr
byn    fi         iu     mn         pt_PT     tt
ca     fo         ja     mo         ro        tt@iqtelif
hacker@commands~an-epic-filesystem-quest:/usr/share/locale$ cat .TIP
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/arch/mips/boot/dts/ralink

The next clue is *delayed* --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/locale$ cd /opt/linux/linux-5.4/arch/mips/boot/dts/ralink
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/mips/boot/dts/ralink$ ls
LEAD              mt7628a.dtsi     rt3050.dtsi      vocore2.dts
Makefile          omega2p.dts      rt3052_eval.dts
mt7620a.dtsi      rt2880.dtsi      rt3883.dtsi
mt7620a_eval.dts  rt2880_eval.dts  rt3883_eval.dts
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/mips/boot/dts/ralink$ cat LEAD
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
```
 
### New Learnings: I learnt patience, how to accurately use all the above mentioned commands completely.

### References : NA


## 11. making directories 

Learning how to make directories and add files to it.

### Solve
**Flag:** ` pwn.college{82K0q__32wKmQYkE_qzj9O-Z94O.01MwMDOxwyM3AzNzEzW}`

###I created a directoy using mkdir command and created a file in it using touch command~
```bash
Connected!
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ ls
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{E4sIktrA1HkphijoPV0SAXinywZ.QXxMDO0wyM3AzNzEzW}
```
 
### New Learnings: I learnt how to make a directory.

### References : Information given in challenge. 


# finding files
The challenge asks me to find all the files in directory, then find flag file inside it

## My solve
**Flag:** `pwn.college{Up6F8g4F_OkiHEFlS7CEp8KS8en.QXyMDO0wSO2EzNzEzW}`

- First I ran `find / -name flag`
- I got a file and used cat to read it
- This gave me the flag

## What I learned
- I learned to find files inside a directory
- How to find all files in /
- How to use -name to specify file name

## References : 
information given in challenge
---

# linking files
To use symlinking to execute a file

## My solve
**Flag:** `pwn.college{gVpo2Xgwx0a5-Zdn3D5XnX4KO-Y.QX5ETN1wyM3AzNzEzW}`
I cd'd to /home/hacker. There I created symbolic link named not-the-flag to refer to flag file. Thus catflag tried to read /home/hacker/not-the-flag; a symbolic link to the /flag.

```bash
hacker@commands~linking-files:~$ cd /home/hacker
hacker@commands~linking-files:~$ ln -s /flag not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{gVpo2Xgwx0a5-Zdn3D5XnX4KO-Y.QX5ETN1wyM3AzNzEzW}
```
## What I learned
- I learnt how to use symlink
- I also learnt difference between soft and hardlink

## References 
 I referred given video andtext in challenge



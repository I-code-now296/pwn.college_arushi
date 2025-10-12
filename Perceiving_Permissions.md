# Linux Luminarium: Perceiving Permissions

## 1. Changing File Ownership
This challenge focuses on the concept of **file ownership** and its role in Linux access control. Files are owned by a single user, and changing this owner using the **`chown`** command is a core method of transferring or seizing control over a file's access rights. Normally restricted to the root user, this level demonstrates how changing a file's owner to the current user can bypass permission restrictions and grant full control.

### Solve
**Flag:** pwn.college{QwYldO3k5v2CFyeL1XuGx8uV3d6.QXxEjN0wyM3AzNzEzW}

changed user, and then cat'd the file to read it. 

### New Learnings
How to change user using chown. 

### References 
referred to given text

---

## 2. Groups and Files
This section introduces group ownership as a mechanism for shared access control in a multi-user environment. A file is owned by both a user and a group. The`chgrp` command is used to change the owning group of a file. By changing a file's group ownership to a group the current user belongs to, the user can gain access based on group-level permissions, even if they are not the file's owner.

### Solve
**Flag:** pwn.college{Ih8UHUWYUAc41W5kcLz0KgOL1bG.QXxcjM1wyM3AzNzEzW}

Changed group to hacker and read fule with cat. 

### New Learnings
you can change group using chgrp <newgroup> <filename>

### References 
referred to given text

---

## 3. Fun With Groups Names
This is a practical application of the **group ownership** concept, emphasizing the need to **identify the user's current groups** before attempting a change. It uses the **`id`** command to dynamically determine the primary group name assigned to the current user, demonstrating that group names are not fixed and must be verified for successful use with commands like `chgrp`.

### Solve
**Flag:** pwn.college{EIlXv1swtE7G6rpLHWgw28MWDeD.QXycjM1wyM3AzNzEzW}

found I was in grp4723 with id. changed group of /flag and checked. 

### New Learnings
most users and in groups same as the user. 

### References 
referred to given text

---

## 4. Changing Permissions
This challenge dives into the core **POSIX file permissions** (read, write, execute), which are divided into three tiers: **User** (owner), **Group**, and **Other** (everyone else). The **`chmod`** command is introduced using the **symbolic mode** (`u+r`, `g-w`, etc.) to modify existing permissions. The concept is that specific access rights can be granted or revoked for different classes of users.

### Solve
**Flag:** pwn.college{k12YAeBsgww068AKhWKmBSGdWfH.QXzcjM1wyM3AzNzEzW}

```
hacker@permissions~changing-permissions:~$ chmod a+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
```

### New Learnings
chmod [OPTIONS] MODE FILE is used to change the permission of each group. Learnt ehat is u, g, o, a

### References 
referred to given text

---

## 5. Executable Files
This section isolates the concept of the **execute permission bit (`x`)**. It highlights that a file must have the execute bit set for the corresponding user class (User, Group, or Other) to be run as a program. Using `chmod`, the necessary execute permission is added to a file, demonstrating the direct link between this permission bit and the operating system's ability to run a file as a binary or script.

### Solve
**Flag:** pwn.college{41_K96NRrlyUEz0IKhnCmBDHOze.QXyEjN0wyM3AzNzEzW}

used `chmod a+c /challenge/run`

### New Learnings
you need to get permission to excecute a file. this is indicated by x.

### References 
referred to given text

---

## 5. Permission Tweaking Practice
This challenge serves as an integrated drill for using **`chmod` in symbolic mode** (`+` and `-`) to incrementally modify permissions. It reinforces the understanding of how to add or remove specific permissions (`r`, `w`, `x`) for specific user classes (`u`, `g`, `o`, `a`) to meet changing access requirements.

### Solve
**Flag:** pwn.college{practice}

solved all 8 succesfully
did chmod +x /flag 
didn't work 
did chmod +r /flag
got this!!


### New Learnings
revised chmod

### References 
referred to given text

---

## Permissions Setting Practice
This challenge advances the use of **`chmod`** by introducing the **absolute setting mode** (`=`) and **chaining multiple modifications** with a comma (`,`). This allows users to completely **overwrite** existing permissions for multiple user classes in a single command (`u=rw,g=r,o=-`), offering powerful and explicit control over a file's access rights.

### Solve
**Flag:** pwn.college{g0kA7yOUF1dYwTadSHIBzFrTjM5.QXzETO0wyM3AzNzEzW}

solved all 8 challenged.

### New Learnings
you can reset the permission of each of the users completely with an equal to symbol.

### References 
referred to given text

---

## The SUID Bit
This challenge introduces the **Set User ID (SUID) bit**, a special permission that enables a program to execute with the **permissions of the file's owner**, rather than the user who executed it. The SUID bit is crucial for system administration tools like `su` and `sudo` and represents a key concept in **privilege escalation**, which is central to many security challenges.

### Solve
**Flag:** pwn.college{0hpvNuv6g3A5FnJ4ul1Wdj6pbgO.QXzEjN0wyM3AzNzEzW}

```
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwsr-xr-x 1 root root 155 Jan 14  2025 /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{0hpvNuv6g3A5FnJ4ul1Wdj6pbgO.QXzEjN0wyM3AzNzEzW}
```

### New Learnings
I learnt SUID
### References 
referred to given text

Sources







# Linux Luminarium: Users

## 1. Becoming root with su
This challenge explores the traditional method of **privilege escalation** using the **`su` (substitute user)** command. Since `su` is a SUID binary, it runs with root privileges, allowing it to start a root shell after successful authentication. The concept demonstrated is the use of a system-wide root password for administrative access, a mechanism now largely considered obsolete.

### Solve
**Flag:** NOT FOUND

Became the root user (using su). To get the flag, I tried reading all the files in root and cat'd the correct sounding files: like myflag and the-flag; but all these flags were wrong.


### New Learnings
WHat is a root user. 

### References 
referred to given text

---

## 2. Other users with su
This section demonstrates the **flexibility of the `su` command** to switch identity to any user, not just the root user. By providing a username as an argument, `su` authenticates with that user's password and launches a new shell with the target user's permissions and environment. This illustrates basic multi-user security boundaries and identity switching.

### Solve
**Flag:** pwn.college{wshu32J738oM67VsHYPmAejkS4h.QX2UDN1wyM3AzNzEzW}

Just typed command `su zardus` to login with user name zardes and ran /challenge/run anfter entering password.


### New Learnings
I learn that the default is root shell but I can give any username to swtich to that user while accessing root. 

### References 
referred to given text

---

## Cracking passwords
This challenge introduces the security concept of **password hashing** and the practice of **password cracking** against leaked shadow files. User password hashes are stored in the restricted `/etc/shadow` file. Since hashing is a one-way process, an attacker with access to these hashes (e.g., through a leak) can use tools like John the Ripper to perform dictionary or brute-force attacks to recover the original cleartext password.

### Solve
**Flag:** pwn.college{8wGd2iRBfLulFCaIRzK-Fm_MCZ_.QX3UDN1wyM3AzNzEzW}

I tried to cat `/challenge/leak`, but zardus password was encrypted, 
So I used john `/challenge/shadow-leak` to get the password 'aardvark'
Then I used that to `su zardok` and ran  `/challenge/run`


### New Learnings
I learnt how to gain access to passwords today with /etc/shadow, the concept of password leaks and the famous John The Ripper for password cracking. 

### References 
referred to given text

---

## Using sudo
This challenge explains the modern and preferred method of **elevated access** using the **`sudo` (substitute user do)** utility. Unlike `su`, which requires a password to launch a new root shell, `sudo` defaults to running a *single command* as root and relies on policy files (`/etc/sudoers`) to determine if the currently logged-in user is authorized. This allows for fine-grained, auditable, and password-less (for the root account) system administration.

### Solve
**Flag:** pwn.college{EpI-0Y5yd-EUSs6T_1m4eqXaBK6.QX4UDN1wyM3AzNzEzW}

Did `sudo /challenge/run`
`sudo cat flag`
etc
got root access but didn't know how to access flag.
so I did ls and tried out all the files with flag in it. 
`sudo cat not-the-flag`

### New Learnings
sudo (substitute user, do), is a common method for system administration and privilege escalation.

### References 
referred to given text


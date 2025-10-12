# Linux Luminarium: Terminal Multiplexing

## 1.Launching Screen
This challenge introduces **terminal multiplexing** via the **`screen`** utility. `screen` creates a persistent, virtual terminal session that runs independently of the user's primary connection. This concept is foundational for managing long-running processes, especially over unstable SSH connections, as the session remains active even if the client disconnects.

### Solve
**Flag:** pwn.college{8IuPSt7gvwm5sruKaEVzZz-sV34.0VN4IDOxwyM3AzNzEzW}

just typed screen and ready through what came up.


### New Learnings
I learnt what a screen is and how to launch. 

### References 
referred to given text

---

## 2. Detaching and Attaching
We understand the core utility of `screen`: s ession persistence. The Ctrl-A followed by d shortcut detaches the session, leaving all running programs active in the background.` screen -r` command allows the user to reattach to the running session, thus to resume work after a connection drop or from a different location.

### Solve
**Flag:** pwn.college{Ypsq8gJso84ZU98-xxAVOhmDmp2.0lN4IDOxwyM3AzNzEzW}

```
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 170.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 170.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
[screen is terminating]
hacker@terminal-multiplexing~detaching-and-attaching:~$
```

### New Learnings
I learn how to detatch a screen without terminating it and how to reattach my screen with screen -r. I even learnt how this can heklp us run something in the background without losing that information.

### References 
referred to given text

---

## 3. Finding Sessions
As users create multiple detached sessions, the ability to list and select them becomes necessary. The`screen -ls` command displays all running `screen` sessions, each identified by a unique ID (PID) and an optional name. The user can then reattach to a specific session by providing its name or ID to the `screen -r` command, managing the complexity of multiple concurrent environments.

### Solve
**Flag:** pwn.college{UbqXxaT6GVJmHC3mUmELp4qHWPW.01N4IDOxwyM3AzNzEzW}

I did ls: 
```
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        144.session_7b117d63cc8c5082    (Detached)
        147.session_10747c6e173beae4    (Detached)
        150.session_6bb6d17592828c8f    (Detached)
3 Sockets in /home/hacker/.screen.
```
my first reattachement gave me the correct screen: `screen -r session_7b117d63cc8c5082`

### New Learnings
You can manage many screens using screens using ls!
you will get an id with every screen. + more details.
you can screen -r to that specific screen.

### References 
referred to given text

---

## 4. Switching Windows
This concept extends multiplexing inside a single `screen` session by allowing multiple **"windows"** (or virtual terminals) to be run concurrently.

### Solve
**Flag:** pwn.college{ElQ4caowUh-PBZvkt148-vfOh-7.0FO4IDOxwyM3AzNzEzW}

I screen -r'd to reattach the screen and then I did crtl + A + 0 top switch from window 1 to window 0 with the flag. 


### New Learnings
- Ctrl-A c - Create a new window
- Ctrl-A n - Next window
- Ctrl-A p - Previous window
- Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9
- Ctrl-A " - bring up a selection menu of all of the windows


### References 
referred to given text

---

## 5. Detaching and Attaching (tmux)
This challenge introduces **`tmux` (terminal multiplexer)**, a modern alternative to `screen` that serves the same function of creating persistent sessions. The core difference is the command prefix, which is **Ctrl-B** for `tmux` shortcuts. The standard commands for listing (**`tmux ls`**) and reattaching (**`tmux attach`** or **`tmux a`**) are also covered.

### Solve
**Flag:** pwn.college{Y9aaFXYnRxz05mrpzIMgltNAXRN.0VO4IDOxwyM3AzNzEzW}


### New Learnings
tmux is a younger cousin. I learnt the tmux, tmux ls, tmux attach commands as well as the crtl + b, crtl + b + d to detatch.

### References 
referred to given text

---

## 6. Switching Windows (tmux)
This final challenge explores **window management within a `tmux` session**. Similar to `screen`, `tmux` allows users to create and navigate multiple windows. The standard `tmux` window shortcuts, such as **Ctrl-B followed by `n` (next)** and **Ctrl-B followed by a number (switch)**, are used to efficiently switch between different executing tasks.

### Solve
**Flag:** pwn.college{MiG4Hixi4JYv0vAC4ca_UhWkFis.0FM5IDOxwyM3AzNzEzW}


### New Learnings
- Ctrl-B c - Create a new window
- Ctrl-B n - Next window
- Ctrl-B p - Previous window
- Ctrl-B 0 through Ctrl-B 9 - Jump to window 0-9
- Ctrl-B w - See a nice window picker

### References 
referred to given text









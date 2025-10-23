# GitHub Codespaces – Linux Command Reference

This quick guide lists a variety of Linux commands you can use inside GitHub Codespaces.
Each command is shown with a short description of what it does.  
Use these to explore your environment, experiment with the terminal, and learn how a cloud-based system works.

---

## 1. Basic Navigation and File Commands
| Command | Description |
|----------|--------------|
| `pwd` | Print the current working directory (shows where you are). |
| `ls` | List files and directories in the current directory. |
| `cd <directory>` | Change into another directory. |
| `mkdir <name>` | Create a new directory. |
| `touch <filename>` | Create a new empty file. |
| `echo "text"` | Print text to the screen. |
| `echo "text" > file.txt` | Write text into a file (overwrites existing content). |
| `cat <filename>` | Display the contents of a file. |
| `grep <text> <file>` | Search for text inside a file. |
| `head <file>` | Show the first ten lines of a file. |
| `tail <file>` | Show the last ten lines of a file (use `tail -f` to follow live logs). |
| `nano <filename>` | Open a simple text editor directly in the terminal. |
|  | Inside nano: **Ctrl + O** to write out (save), **Enter** to confirm filename, and **Ctrl + X** to exit. |
| `cp <source> <destination>` | Copy a file or directory. |
| `mv <source> <destination>` | Move or rename a file or directory. |
| `rm <filename>` | Delete a file. |
| `rmdir <directory>` | Delete an empty directory. |
| `clear` | Clear the terminal window. |
| `history` | Show a list of previously entered commands. |
| `man <command>` | Show help information (manual page) for a command. |
| `exit` | Close the terminal session. |

---

## 2. System and Environment Information
| Command | Description |
|----------|--------------|
| `whoami` | Display the current username. |
| `uname -a` | Show kernel and operating-system information. |
| `lsb_release -a` | Show Linux distribution details. (LSB stands for Linux Standard Base.) |
| `cat /etc/os-release` | Display operating-system version information. |
| `hostname` | Show the name of the machine. |
| `echo $CODESPACE_NAME` | Print the Codespaces environment name (if set). |
| `env \| grep CODESPACE` | List environment variables related to Codespaces. |
| `df -h` | Show disk usage and available space. |
| `uptime` | Display how long the system has been running. |
| `top` | Show running processes and resource usage. |

---

## 3. Networking and Connectivity
| Command | Description |
|----------|--------------|
| `curl -I https://example.com` | Fetch only the HTTP headers from a website. |
| `ip addr` | Show network interfaces and their IP addresses. |
| `ifconfig` | Alternative command for viewing network interfaces (older syntax). |
| `ss -tuln` | Display active network sockets and listening ports. |

---

## 4. Extra Commands to Explore

The following are additional Linux commands you can try in your Codespace.  
Some provide useful system information, others perform basic utilities, and a few may depend on what software is installed.  
Experiment with them and observe what happens.

| Command | Description |
|----------|-------------|
| `vi <filename>` / `vim <filename>` | Open the traditional terminal text editor (`:wq` to save and exit). |
| `uname -r` | Show only the kernel version. |
| `ps aux` | Display all running processes. |
| `free -h` | Show memory usage in human-readable format. |
| `uptime -p` | Show how long the system has been running in plain English. |
| `df -Th` | Display filesystems and their types, with sizes and usage. |
| `sudo apt list --installed` | List all installed packages. |
| `date` | Show the current system date and time. |
| `cal` | Display a calendar for the current month. |
| `startx` | Start a graphical desktop session. |
| `which python3` | Show the location of a program or command. |
| `echo $SHELL` | Display which command shell is currently in use. |
| `echo $DISPLAY` | Print the current display identifier used for graphical sessions. |

---

### Notes
- Most commands can be combined with the `--help` option for more details.  
- Some commands may not be installed by default in your Codespace.  
  If you see “command not found,” you can usually install the missing package with  
  `sudo apt-get update` followed by `sudo apt-get install <package>`.  
  For example: the `cal` command is provided by the `ncal` package. 
- The `clear` command does not erase anything—it only resets the visible terminal window.  
- You can use **Ctrl +C** to stop most commands that keep running (e.g., `ping` without a `-c` count).  

---

# 🐧 Basic Linux Commands Cheat Sheet

## Core Commands
Hey newbie! Here is a list of which will get you started with mastering your Linux! I know it might look bit intimidating, but best way to learn is to try them out!
So open up your Linux terminal and get to it, go through the commands and see what they do! H-T8 also gives you couple of tasks to do in this manual after you studied a bit

| Command       | Description                                | Example Usage                                   |
|---------------|--------------------------------------------|-------------------------------------------------|
| `ls`          | List directory contents                    | `ls -l /home/santeri`                           |
| `cd`          | Change directory to                        | `cd /var/log`                                   |
| `pwd`         | Show current directory path                | `pwd`                                           |
| `cat`         | Display contents of a file                 | `cat notes.txt`                                 |
| `less`        | View file one page at a time               | `less longfile.txt`                             |
| `grep`        | Search for patterns in files               | `grep 'error' /var/log/syslog`                  |
| `find`        | Search for files and directories           | `find /home -name "*.txt"`                      |
| `wget`        | Download files from the web                | `wget http://example.com/file.zip`              |
| `curl`        | Transfer data from or to a server          | `curl -O http://example.com/file.zip`           |
| `nc` (netcat) | Network tool (port scanning, chat, etc.)   | `nc -v -z 192.168.0.1 1-1000`                    |

## Bonus Essentials

| Command       | Description                                | Example Usage                                   |
|---------------|--------------------------------------------|-------------------------------------------------|
| `echo`        | Print text to terminal                     | `echo "Hello, hacking club!"`                   |
| `man`         | Show manual/help for a command             | `man grep`                                      |
| `chmod`       | Change file permissions                    | `chmod +x script.sh`                            |
| `chown`       | Change file ownership                      | `chown santeri:santeri notes.txt`              |
| `mkdir`       | Make a new directory                       | `mkdir projects`                                |
| `rm`          | Remove a file or directory                 | `rm old_file.txt` or `rm -r old_folder`         |
| `cp`          | Copy files and directories                 | `cp file.txt backup.txt`                        |
| `mv`          | Move or rename files                       | `mv file.txt archive.txt`                       |
| `whoami`      | Show your current username                 | `whoami`                                        |
| `top`         | Real-time system resource usage            | `top`                                           |
| `ps`          | Show running processes                     | `ps aux | grep firefox`                         `

## TASKS

Here you get to put what you learned to the test, and well actually start learning. Skills is not just reading and remembering. It´s also failing and finding out!

### Head to this website! 

https://overthewire.org/wargames/bandit/bandit0.html

Complete tasks 0-8. After you completed these you will see significant improvement on understanding The Penguins secrets!

### Yay good job you!

# 🌐 Beginner-Friendly Networking Tools for Linux

This section introduces you to common command-line tools to check and explore networks. No experience needed—just curiosity!

---

## 🔍 1. `ping` — Test if a computer is reachable

- **What it does:** Sends a small message to another computer to see if it's online and how fast the response is.
- **Why it's useful:** You can check if your internet is working, or if a specific website or device is reachable.

### Example:
```bash
ping google.com
```

### What it might show:
```text
PING google.com (142.250.200.142) 56(84) bytes of data.
64 bytes from 142.250.200.142: icmp_seq=1 ttl=117 time=20.4 ms
64 bytes from 142.250.200.142: icmp_seq=2 ttl=117 time=21.1 ms
```

---

## 📄 2. `ip a` — Show your computer’s IP address

- **What it does:** Displays all network interfaces and their IP addresses.
- **Why it's useful:** You’ll need this to find your local IP address, especially for LAN scanning.

### Example:
```bash
ip a
```

### What it might show:
```text
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> ...
    inet 192.168.1.42/24 brd 192.168.1.255 scope global dynamic eth0
```

---

## 📊 3. `netstat` or `ss` — See open ports and connections

- **What it does:** Lists the network connections your computer is making and ports it's listening on.
- **Why it's useful:** Useful for spotting unexpected programs connecting to the internet or checking if your server is running.

### Example:
```bash
netstat -tulnp
```

### What it might show:
```text
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      743/sshd
udp        0      0 0.0.0.0:68              0.0.0.0:*                           644/dhclient
```

---

## 🔎 4. `nmap` — Scan other computers on the network

- **What it does:** Checks what ports are open on a remote computer and tries to guess what services are running.
- **Why it's useful:** Helps you understand what other machines are doing and if they might be vulnerable.

### Example:
```bash
nmap -sV 192.168.1.10
```

### What it might show:
```text
PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 8.2
80/tcp   open  http     Apache httpd 2.4.41
```

---

## 👀 5. `arp-scan` — Discover devices on your local network

- **What it does:** Finds every device connected to the same Wi-Fi or LAN.
- **Why it's useful:** Great way to see who’s sharing your network—even hidden or unnamed devices.

### Example:
```bash
sudo arp-scan --interface=eth0 --localnet
```

### What it might show:
```text
192.168.1.1  00:11:22:33:44:55  TP-Link Technologies
192.168.1.42 00:0c:29:ab:cd:ef  Raspberry Pi Foundation
```

---

## 🧠 Bonus Tools

### 💬 `traceroute` — Follow the path to a website

- **What it does:** Shows every server your data passes through on its way to a website.
- **Why it’s cool:** Helps spot where network delays or issues might be happening.

```bash
traceroute example.com
```

---

### 🌐 `dig` or `nslookup` — Check domain name info (DNS)

- **What it does:** Asks the internet’s “phone book” what IP address a domain (like `bing.com`) uses.
- **Why it matters:** Understanding DNS is key to how the web works.

```bash
dig microsoft.com
```

---

### 📥 `tcpdump` — Capture all network traffic (advanced)

- **What it does:** Records packets (tiny data chunks) going in and out of your computer.
- **Why it matters:** Very powerful for analyzing or debugging network behavior.

```bash
sudo tcpdump -i eth0
```

---

## TASKS

Get back to overthewire and complete exercises 14-20! (I know you need to complete 9-13 before you get the password to get here, but greatness has never been without a cost!

# ⚠️ _Reminder: Always get permission before scanning or sniffing any network. Stick to school labs, virtual machines, or your own LAN._


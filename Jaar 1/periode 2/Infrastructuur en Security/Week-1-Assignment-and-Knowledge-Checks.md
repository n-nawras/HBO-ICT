
# Exploring Linux Commands and Network Connectivity

**Exploring Linux Commands and Network Connectivity** involves understanding how to use Linux's command-line interface (CLI) to perform tasks related to system management and network troubleshooting. Here's a breakdown:

---

## Basic Linux Commands

Linux provides a powerful CLI to interact with the system. Key commands include:

### 1. File and Directory Management
- `ls`: Lists files in a directory.
  - Example: `ls -l` shows detailed information.
- `cd`: Changes directories.
  - Example: `cd /home/user/Documents` navigates to the Documents folder.
- `mkdir`: Creates directories.
  - Example: `mkdir new_folder`.
- `rm`: Removes files or directories.
  - Example: `rm file.txt` removes a file, while `rm -r folder` removes a folder and its contents.

### 2. File Viewing and Editing
- `cat`: Displays file contents.
  - Example: `cat file.txt`.
- `nano`/`vim`: Edits files directly from the terminal.
  - Example: `nano file.txt` opens a file in the Nano editor.
- `less`: Opens a file for viewing (scrollable).
  - Example: `less file.txt`.

### 3. Process Management
- `ps`: Lists running processes.
  - Example: `ps aux` shows all processes with details.
- `top`/`htop`: Displays real-time process information.
- `kill`: Terminates a process.
  - Example: `kill 1234` stops the process with ID 1234.

### 4. System Information
- `uname -a`: Displays system information.
- `df -h`: Shows disk space usage.
- `free -h`: Shows memory usage.

---

## Network Connectivity Commands

These commands help manage and troubleshoot network connections:

### 1. Checking Connectivity
- `ping`: Tests connectivity to a host.
  - Example: `ping google.com`.
- `curl`/`wget`: Fetches web content.
  - Example: `curl https://example.com`.

### 2. Viewing Network Configuration
- `ip a`: Displays IP addresses and interfaces.
- `ifconfig` (deprecated, but still used): Shows network interfaces and settings.
- `nmcli`: Manages network configurations (e.g., with NetworkManager).

### 3. Diagnosing Network Issues
- `traceroute`: Shows the path packets take to a destination.
  - Example: `traceroute google.com`.
- `netstat`/`ss`: Displays active connections and listening ports.
  - Example: `ss -tuln` lists all open ports.

### 4. Managing Network Connections
- `nmcli`: Connects to or disconnects from networks.
  - Example: `nmcli device wifi list` shows available Wi-Fi networks.
- `ip link set`: Brings interfaces up or down.
  - Example: `ip link set eth0 up`.

---

## Combining Commands for Network Analysis

Linux allows combining commands for advanced tasks. Examples:

- Check connectivity and log results:
  ```bash
  ping -c 4 google.com > ping_log.txt
  ```

- Monitor network traffic in real time:
  ```bash
  sudo tcpdump
  ```

- Troubleshoot DNS issues:
  ```bash
  dig example.com
  ```

---

## Practice and Exploration

The best way to learn is by hands-on experimentation. Use a Linux system or virtual machine to try out these commands. If you're unsure about any command's functionality, use `man` (manual):

```bash
man command_name
```

For example, `man ping` provides detailed information on the `ping` command.

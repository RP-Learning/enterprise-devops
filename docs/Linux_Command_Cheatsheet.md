Linux Command Cheatsheet (Foundations)
# Linux Command Cheatsheet – Foundations

This file contains essential Linux commands with clear explanations.
These commands cover environment awareness, filesystem navigation,
permissions, process management, CPU/memory inspection, and safe operations.

---

## Environment & Context Awareness
Always know who you are and where you are before running commands.

```bash
whoami          # Shows the current logged-in user
hostname        # Displays the system hostname
uname -a        # Shows kernel and OS details
pwd             # Prints the current working directory

Filesystem Navigation

Used to move around and inspect directories.

ls              # Lists files and directories
ls -la          # Lists all files with permissions and ownership
cd /            # Moves to the root directory
cd ~            # Moves to the current user's home directory

Disk Usage & Capacity

Used to understand storage consumption.

df -h            # Shows disk space usage of mounted filesystems
du -sh /etc      # Shows size of /etc directory
du -sh /var      # Shows size of /var directory
du -sh /home     # Shows size of /home directory
du -sh /* 2>/dev/null
                 # Shows size of root directories while suppressing permission errors

Important System Directories

Used to inspect core parts of the Linux filesystem.

ls /etc         # Lists configuration files
ls /var/log     # Lists system and application logs
ls /bin         # Lists essential system binaries
ls /usr/bin     # Lists user-level binaries
ls /proc        # Lists kernel and process information (virtual filesystem)

File & Binary Inspection

Used to inspect file metadata and types.

stat /etc/passwd    # Displays detailed metadata of a file
file /bin/bash     # Identifies file type (binary, script, text, etc.)
which bash          # Shows the path of the executable being used

Permissions & Ownership

Used to control access to files and scripts.

ls -l               # Displays permissions and ownership
chmod 644 file      # Sets read-write for owner, read-only for others
chmod 755 file      # Adds execute permission (used for scripts/binaries)

Process Inspection (Snapshot View)

Used to see what is running on the system.

ps                  # Shows processes in the current shell session
ps aux              # Shows all processes with CPU and memory usage
ps -ef              # Shows all processes in full-format view
ps aux | grep nginx # Filters process list to find a specific process

Real-Time Process Monitoring

Used during live incidents.

top                 # Real-time process and resource monitoring
htop                # Enhanced interactive process viewer (if installed)


Inside top:

P → sort by CPU usage

M → sort by memory usage

q → quit

CPU & Load Inspection

Used to understand system performance and contention.

lscpu               # Displays CPU architecture and details
nproc               # Shows number of CPU cores
uptime              # Shows system uptime and load average

Memory Inspection

Used to diagnose memory pressure.

free -h             # Shows memory usage in human-readable format
vmstat              # Displays memory, CPU, and IO statistics

/proc Process Inspection

Used for deep debugging of running processes.

ls /proc/<PID>              # Lists process-specific kernel data
cat /proc/<PID>/status      # Shows process state and memory usage
cat /proc/<PID>/cmdline     # Shows how the process was started

Signals & Process Control

Used to stop or control processes safely.

kill <PID>          # Sends SIGTERM (graceful shutdown)
kill -9 <PID>       # Sends SIGKILL (force kill – last resort only)

Command History & Audit

Used for traceability and debugging.

history             # Shows command history
history | tail      # Shows the most recent commands

Git Discipline

Used to track and version changes.

git status          # Shows repository status
git add .           # Stages changes
git commit -m "msg" # Commits changes with message
git push            # Pushes commits to remote repository

Key Best Practices

Always check context using pwd

Prefer absolute paths in scripts

Avoid blind sudo

Use ps for snapshots, top for live analysis

Prefer SIGTERM over SIGKILL

Treat permission errors as signals, not failures.

# Day 1 – Linux Filesystem & Permissions

## What I Learned
- Linux filesystem hierarchy and purpose of core directories
- Difference between relative and absolute paths
- Linux file permissions and ownership model
- Why permission issues commonly cause production failures

## Why This Matters in Production
- Linux systems strictly enforce permissions to protect system integrity
- Applications depend on correct configuration, log access, and execution rights
- Misconfigured paths or permissions can prevent services from starting
- Understanding filesystem layout helps debug incidents faster

## Key Directories Understood
- /etc – System-wide and application configuration files
- /var/log – Application and system logs used for troubleshooting
- /home – User data and workspaces
- /bin, /usr/bin – Core binaries and executables
- /proc – Virtual filesystem exposing kernel and process information

## Key Commands Practiced
- ls, ls -la, pwd, cd
- du, df
- stat, file, which
- chmod, chown

## Mental Model Gained
- Linux enforces least-privilege access by default
- Absolute paths should be preferred in scripts and production work
- Permission and path issues are among the most common causes of outages


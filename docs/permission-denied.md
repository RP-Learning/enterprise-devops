# Permission Denied While Running du -sh /*

## Problem
Running `du -sh /*` resulted in multiple "Permission denied" errors.

## Root Cause
Some system directories such as /root, /proc, /sys, and parts of /var are restricted to root users. Linux prevents non-root users from traversing these paths to enforce security and least-privilege access.

## Fix / Workaround
- Suppressed permission errors using:
  du -sh /* 2>/dev/null
- Or selectively ran du on known safe directories:
  du -sh /etc /var /home /usr

## Lesson Learned
- Permission denied errors are expected behavior, not failures
- Blindly using sudo is unsafe and discouraged
- Understanding filesystem protection is critical for secure operations

## Interview Explanation
"Permission denied occurs because Linux restricts access to sensitive system directories. I either suppress errors or elevate privileges only when required, following least-privilege principles."


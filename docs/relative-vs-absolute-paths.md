# Relative vs Absolute Path Confusion

## Problem
Commands like `cd boot` and `cd etc` failed with "No such file or directory".

## Root Cause
I was inside `/home/<user>/enterprise-devops/docs`. Relative paths search inside the current directory, while `boot` and `etc` exist at the root filesystem level.

## Fix
Used absolute paths:
- cd /boot
- cd /etc
- cd /var/log

## Lesson Learned
- Always confirm the current directory using `pwd`
- Relative paths depend on execution context
- Absolute paths are safer for scripts and production systems

## Interview Explanation
"Relative paths depend on the current working directory, while absolute paths start from /. In production scripts, I prefer absolute paths to avoid ambiguity."


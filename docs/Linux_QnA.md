# Linux Interview Questions & Answers – Foundations

---

## Why is /etc critical in production systems?
/etc contains system-wide and application configuration files. Production services depend on these configurations, and incorrect values or permissions can prevent services from starting or cause outages.

---

## Why is /var/log the first place to check during incidents?
/var/log contains system and application logs that capture runtime behavior. Logs help reconstruct timelines and identify failures during incidents.

---

## What is the difference between chmod 644 and chmod 755?
644 allows read-write access for the owner and read-only access for group and others.  
755 adds execute permission, which is required for scripts and binaries.

---

## Why do permission issues cause application failures?
Applications fail when they cannot read configuration files, write logs, or execute binaries. Linux strictly enforces permissions to ensure correctness and security.

---

## What does /proc represent?
/proc is a virtual filesystem that exposes real-time kernel and process information such as CPU usage, memory state, and process details.

---

## What is a process?
A process is a running instance of a program with a unique PID, ownership, and allocated system resources.

---

## Why does the USER column matter in ps output?
It shows which account owns a process. Permissions, access, and security policies depend on user context.

---

## Difference between ps and top?
ps shows a snapshot of processes at a specific moment.  
top shows real-time process activity and is preferred during live incidents.

---

## What does load average indicate?
Load average represents the number of processes waiting for CPU or I/O resources. High load indicates contention.

---

## Why does Linux show low free memory?
Linux uses available memory for caching to improve performance. Cached memory is released when applications need it.

---

## Difference between used and available memory?
Used memory includes cache, while available memory indicates how much memory can be allocated without swapping.

---

## What does /proc/<pid> show?
It exposes real-time information about a specific process, including state, memory usage, and command-line arguments.

---

## Difference between SIGTERM and SIGKILL?
SIGTERM allows graceful shutdown and cleanup.  
SIGKILL forcefully terminates a process without cleanup.

---

## Why is kill -9 dangerous?
It bypasses cleanup logic and can cause data corruption or inconsistent system state.

---

## How do you investigate high CPU or memory usage?
By inspecting processes using ps and top, checking load and memory availability, and applying graceful remediation.

---



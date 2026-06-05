# Day 01 — Filesystem Navigation

## Scenario
First day as a junior sysadmin. A senior engineer asks you to find the main config directory and the log directory on a Linux server and report what's in them.

## Requirements Completed
1. Print current location
2. List the root directory `/`
3. Navigate into `/etc` and list its contents
4. Navigate into `/var/log` and list its contents
5. Return home in a single command
6. Display full path of home directory

## Commands Used

```bash
# 1. Print current location
pwd
# Output: /home/biroue

# 2. List root directory (long format + hidden files)
ls -al /

# 3. Navigate to /etc and list contents
cd /etc
ls

# 4. Navigate to /var/log and list contents
cd /var/log
ls

# 5. Return home in one command
cd

# 6. Confirm home directory
pwd
# Output: /home/biroue
```

## Key Directories Learned

| Directory | Purpose |
|-----------|---------|
| `/etc` | System-wide configuration files |
| `/var/log` | Log files (system, services, security) |
| `/home` | User home directories |
| `/bin` → `/usr/bin` | Commands and programs (symlink on RHEL 9) |
| `/tmp` | Temporary files, cleared on reboot |
| `/proc`, `/sys` | Virtual filesystems — live kernel data, not real files on disk |

## What I Learned
- The Linux filesystem is one tree rooted at `/` — there are no drive letters like Windows.
- `pwd` tells you where you are; your shell prompt also shows your location (`~` means home).
- `cd` with no arguments always returns you to your home directory.
- `/etc` is the first place to look when configuring a service; `/var/log` is the first place to look when something breaks.
- `ls -al` shows hidden files (starting with `.`) and detailed metadata like permissions and ownership — more useful than plain `ls`.

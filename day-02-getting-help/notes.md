# Day 02 — Getting Help & Reading Man Pages

## Scenario
On a production server with no internet access, you need to look up command options and find the right tool for a job — using only the system's built-in help.

## Requirements Completed
1. Find the option in `man ls` that sorts by modification time
2. Find the option in `man cp` that copies directories recursively
3. Use `man hier` to find the official description of `/tmp`
4. Use `--help` on a command of choice
5. Use `apropos` to search for commands related to passwords

## Commands Used

```bash
# 1. Sort by modification time
man ls
# Found: --time=mtime (or -t)

# 2. Copy directories recursively
man cp
# Found: -R, -r, --recursive

# 3. Official description of /tmp
man hier
# Found: "This directory contains temporary files which may be deleted
#         with no notice, such as by a regular job or at system boot up."

# 4. Quick help output
ls --help

# 5. Search for password-related commands
apropos passwd
```

## Key Findings

| Command | Option | Meaning |
|---------|--------|---------|
| `ls` | `--time=mtime` or `-t` | Sort by modification time |
| `cp` | `-r` / `-R` / `--recursive` | Copy directories recursively |

## Man Page Sections

| Section | Content |
|---------|---------|
| 1 | User commands (e.g. `passwd(1)`) |
| 5 | File formats (e.g. `passwd(5)`) |
| 8 | Admin/root commands (e.g. `chpasswd(8)`) |

Open a specific section with: `man 5 passwd`

## Navigation Inside a Man Page

| Key | Action |
|-----|--------|
| Arrow keys / Space | Scroll |
| `/word` | Search for "word" |
| `n` | Next match |
| `q` | Quit |

## What I Learned
- `man` is the offline reference manual — the only resource allowed on the RHCSA exam.
- `apropos` finds commands by keyword when you don't know the exact command name.
- `--help` is faster for a quick reminder; `man` is for full detail.
- The same name can appear in multiple man sections (e.g. `passwd(1)` vs `passwd(5)`) — use `man <section> <name>` to open the right one.
- My system uses a French locale — on the exam the system will be in English. Use `LANG=C <command> --help` to force English output.

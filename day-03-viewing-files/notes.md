# Day 03 — Viewing & Creating Files

## Scenario
A colleague left notes in a config file on the server. You need to read it, check its size, and create files of your own — all from the command line without a text editor.

## Requirements Completed
1. Create a file with a specific line of text
2. Display the file contents
3. Append a second line without overwriting
4. Confirm both lines are present
5. Count the number of lines
6. Create an empty file
7. Display only the last line

## Commands Used

```bash
# 1. Create file with first line
echo "I am learning RHCSA" > sysadmin.txt

# 2. Display contents
cat sysadmin.txt
# Output:
# I am learning RHCSA

# 3. Append second line (>> not > !)
echo "Linux is powerful" >> sysadmin.txt

# 4. Confirm both lines
cat sysadmin.txt
# Output:
# I am learning RHCSA
# Linux is powerful

# 5. Count lines
wc -l sysadmin.txt
# Output: 2 sysadmin.txt

# 6. Create empty file
touch placeholder.txt

# 7. Show last 1 line
tail -n 1 sysadmin.txt
# Output: Linux is powerful
```

## Critical Distinction: > vs >>

| Operator | Behaviour | Risk |
|----------|-----------|------|
| `>` | Overwrites the file | Destroys existing content |
| `>>` | Appends to the file | Safe — adds to the end |

**Exam trap:** using `>` when you meant `>>` silently destroys data with no warning.

## Commands Reference

| Command | Purpose |
|---------|---------|
| `echo "text"` | Print text to screen (or redirect to file) |
| `cat file` | Display file contents |
| `wc -l file` | Count lines in a file |
| `touch file` | Create empty file or update timestamp |
| `tail -n N file` | Show last N lines of a file |

## What I Learned
- `>` overwrites, `>>` appends — this distinction is critical and a common exam trap.
- `echo` combined with redirection is the fastest way to write to files from the command line.
- `touch` creates an empty file instantly — useful for placeholders or triggering timestamp updates.
- `tail -n 1` is handy for quickly checking the end of log files.

# RHCSA Lab — EX200 Study Journal

> **Red Hat Certified System Administrator (RHEL 9) — hands-on daily practice log**

A daily, task-by-task journey from Linux beginner to RHCSA-certified system administrator.
Every folder documents a real task completed and verified on a live RHEL/Linux system.

---

## About This Repo

I am studying for the **RHCSA EX200** exam (RHEL 9). This repo is my public practice log:
- One folder per completed task
- Each folder contains `notes.md`: the scenario, commands used, output, and what I learned
- Difficulty increases progressively, following the official RHCSA curriculum

**Goal:** Pass the EX200 exam and build the hands-on Linux foundation needed for a system engineering career.

---

## Progress Tracker

| # | Topic | Difficulty | Status |
|---|-------|-----------|--------|
| [Day 01](day-01-filesystem-navigation/) | Filesystem navigation & hierarchy | ★☆☆☆☆ | ✅ Done |

---

## Curriculum Roadmap

1. **Foundations** — navigation, filesystem hierarchy, help systems
2. **Text & I/O** — vim, redirection, pipes
3. **Users & Permissions** — users, groups, ACLs, special bits
4. **Processes & Services** — systemd, journald, jobs
5. **Package Management** — dnf, repos, modules
6. **Storage** — partitions, filesystems, fstab, swap
7. **LVM** — physical volumes, volume groups, logical volumes
8. **Networking** — nmcli, hostname, firewalld
9. **SSH** — key-based authentication
10. **Scheduling** — cron, at, systemd timers
11. **SELinux** — modes, contexts, booleans, troubleshooting
12. **Advanced** — podman, Stratis, tuning, autofs
13. **Mock Exams** — full timed scenarios

---

## Repo Structure

```
rhcsa-lab/
├── README.md               ← this file (progress index)
├── cheatsheets/            ← growing reference cards by topic
└── day-NN-topic/
    └── notes.md            ← scenario, commands, output, lessons learned
```

---

## Commit Convention

```
day-01: complete filesystem navigation task
day-07: fix: correct fstab entry for persistent mount
cheatsheet: add vim basics reference
```

---

*Consistency over perfection. One task a day.*

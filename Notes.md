# Linux Home Lab Notes

This file documents my progress while learning Linux in Oracle VirtualBox. These notes record the commands I practiced, problems I encountered, how I solved them, and the skills I gained throughout the project.

---

# July 29, 2026

## Objective
Install Ubuntu Desktop in Oracle VirtualBox and configure a stable Linux virtual machine.

## Tasks Completed
- Installed Ubuntu Desktop in Oracle VirtualBox.
- Configured VirtualBox settings for Ubuntu.
- Booted into Ubuntu for the first time.

## Problems Encountered
- Ubuntu displayed a black screen during boot.
- Received a `vmwgfx` unsupported hypervisor error.
- Experienced an `rcu_preempt self-detected stall on CPU` kernel panic.

## How I Solved It
- Disabled Windows Hyper-V.
- Disabled Windows Core Isolation.
- Verified virtualization (VT-x/AMD-V) was enabled in BIOS.
- Switched the graphics controller to **VMSVGA**.
- Increased video memory.
- Disabled 3D acceleration.
- Booted Ubuntu using the `nomodeset` kernel parameter.

## What I Learned
- Hyper-V can interfere with VirtualBox.
- Virtual machine display settings can prevent Linux from booting.
- GRUB boot parameters are useful for troubleshooting Linux startup issues.

---

# July 30, 2026

## Objective
Practice Linux navigation and basic file management.

## Commands Practiced
- pwd
- ls
- ls -l
- cd
- mkdir
- touch
- nano
- cat
- cp
- mv
- rm

## Tasks Completed
- Created directories and files.
- Edited files using Nano.
- Copied files with `cp`.
- Moved files using `mv`.
- Deleted files using `rm`.
- Displayed file contents using `cat`.
- Organized files into a Practice directory.

## Problems Encountered
- Forgot to include a destination when using `cp`.
- Accidentally deleted `notes.txt`.

## How I Solved It
- Learned that `cp` requires both a source and destination.
- Restored the deleted file using a backup copy.

## What I Learned
- Basic Linux file management.
- The importance of creating backups before deleting files.
- How to read and understand Linux error messages.

---

# August 3, 2026

## Objective
Learn Linux permissions, administrative commands, networking, and Linux documentation.

## Commands Practiced
- chmod
- sudo
- apt update
- history
- man
- ping
- ip a

## Tasks Completed
- Updated package information using `sudo apt update`.
- Changed file permissions using `chmod`.
- Removed and restored read permissions on a file.
- Created a protected directory and tested directory permissions.
- Used `history` to review previous commands.
- Read Linux documentation using `man ping`.
- Tested internet connectivity with `ping`.
- Displayed network information using `ip a`.

## Problems Encountered
- Received a **Permission denied** error after removing read permissions from `hidden.txt`.
- Initially entered the `ping` command incorrectly.

## How I Solved It
- Restored file permissions with `chmod`.
- Corrected the syntax by using:

```bash
ping -c 4 google.com
```

## Results
- Successfully received replies from google.com with **0% packet loss**.
- Confirmed the VM had an IPv4 address assigned on interface `enp0s3`.
- Successfully updated Ubuntu package lists.

## What I Learned
- Linux permissions control who can read, write, and execute files.
- `sudo` allows administrative access.
- `history` displays previously executed commands.
- `man` provides built-in Linux documentation.
- `ping` tests network connectivity and DNS resolution.
- `ip a` displays network interfaces and IP addresses.

---

# Commands Learned

## Navigation
- pwd
- ls
- ls -l
- cd

## File Management
- mkdir
- touch
- nano
- cat
- cp
- mv
- rm

## Permissions
- chmod

## Administration
- sudo
- apt update

## Networking
- ip a
- ping

## Help & Documentation
- man
- history

---

# Skills Gained

- Linux command-line navigation
- File and directory management
- File permissions
- Package management
- Basic networking
- Virtual machine management
- Linux troubleshooting
- Reading Linux documentation
- Problem-solving through command-line errors

---

# Next Project

## Two-VM Networking Lab

### Goals
- Create a second Ubuntu virtual machine.
- Configure communication between both VMs.
- Learn SSH.
- Configure firewall rules with UFW.
- Capture network traffic using Wireshark.
- Document the entire project on GitHub.

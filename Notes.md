# Linux Home Lab Notes

Documenting my self-directed Linux home lab, built in VirtualBox, to build 
practical skills in Linux commands, file management, and systems 
administration — in preparation for transferring into NC A&T's Information 
Systems program.

---

## July 29, 2026

Today I focused on setting up Ubuntu Desktop in VirtualBox and resolving 
hypervisor and kernel boot issues.

### Tasks Completed
- Configured VirtualBox VM parameters for a modern Linux guest.
- Troubleshot kernel boot flags and display driver errors to achieve a 
  stable desktop boot.

### Problems I Encountered
- **Hypervisor / Display Driver Error:** Upon booting Ubuntu, the VM 
  appeared to be running on an unsupported hypervisor configuration, 
  which caused a black screen on boot.
- **Kernel / CPU Stalls:** The VM locked up completely with a kernel 
  panic: `rcu: INFO: rcu_preempt self-detected stall on CPU`.

### How I Solved It
- **Hypervisor Conflicts:** Disabled Windows Hyper-V 
  (`bcdedit /set hypervisorlaunchtype off` and turning off Core Isolation), 
  and confirmed hardware virtualization was enabled in BIOS.
- **Display Driver Conflict:** Configured VirtualBox display settings to 
  use the `VMSVGA` graphics controller, increased allocated video memory, 
  and disabled 3D acceleration.
- **Black Screen Fix:** Appended `nomodeset` as a kernel boot parameter 
  (via GRUB) to force a basic framebuffer during setup.

---

## July 30, 2026

Today I continued working in Ubuntu Desktop using VirtualBox, focusing on 
core file management commands.

### Tasks Completed
- Created a `practice` directory.
- Created a `notes.txt` file.
- Edited files using `nano`.
- Copied files using `cp`.
- Moved files into the practice directory using `mv`.
- Deleted a file using `rm`.
- Verified file contents using `cat`.

### Problems I Encountered
I initially used the `cp` command incorrectly and received an error 
because I didn't specify a destination. Later, I accidentally deleted 
`notes.txt` after making a backup.

### How I Solved It
I learned that `cp` requires both a source and a destination. Because I 
had already created `backup.txt`, I was able to restore the deleted file 
by copying it back with `cp backup.txt notes.txt`.

### What I Learned
- Basic command-line file operations: `mkdir`, `touch`, `cd`, `pwd`, 
  `nano`, `cp`, `mv`, `rm`, `cat`.
- The importance of keeping a backup before modifying or deleting a file.

### Next Goals
- `chmod` — file permissions
- `sudo` — admin privileges
- `ip` — network interface configuration
- `ping` — network connectivity testing

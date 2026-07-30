# linux_home_lab_notes
Linux home lab built in VirtualBox to learn Linux commands, file management, and systems, adminstration fundamentals.

## July 29, 2026
Today I focused on setting up Ubuntu Desktopin VirtualBox and Resolving hypervisor and kernel boot issues.

### Tasks Completed 
- Configured VirtualBox VM parameters for modern Linux guest.
- Troubleshot kernel boot flags and display driver errors to achieve a stable desktop boot.

### Problems I Encountered
- **Hypervisor / Display Driver Error :** Upon booting Ubuntu, the VM seem to be running on a unsupported hypervisor that would cause a black screen on boot.
- **Kernel / Cpu stalls:** The VM locked up completely with a kernel panic : 'rcu:INFO rcu_preempt self-dected stall on CPU'

### How I solved it 
- **Hypervisor Conflicts:** Disabled WIndows Hyper-V ('bcdedit /sethypervisolaunchtype off' and turning off Core isolation) and confrimed hardware virualization in bios.
- **Display Driver Conflict:** Configured the VirtualBox display settings to use the 'VMSVGA' graphic controlled, allowed more memory, and disabled 3d acceleration.
- **Black Screen Fix:** Appended 'nomodeset' to GRUB boot arguements to force an basio framebuffer during setup.

---

## July 30, 2026
Today I continued working in Ubuntu Desktop using VirtualBox.

### Tasks Completed
- Created a Practice directory
- Created a notes.txt
- Edited files using nano.
- Copied the files using cp
- Moved files into practice directory
- Deleted a file using rm
- Verified file contents using cat

### Problems I encountered
I initially used the cp command incorrectly and received a error because I didn't specify a destination.
Later, I accidentally deleted notes.txt after making a backup.
## How I solved It
I learned that the cp command required both a source and destination.
Because I had already created backup.txt, I could restore the deleted file by copying it back.

### What I Learned
-  Basic command-line file operations ( 'mkdir','touch','cd','pwd','nano','cp','mv','rm','cat')
-  The importance of keeping a backup of a file before modifying or deleting it
### Next Goal
Learn
- chmod [file permission]
- sudo [admin privileges]
- ip [networking interfacing]
- ping [network connectivity testing]

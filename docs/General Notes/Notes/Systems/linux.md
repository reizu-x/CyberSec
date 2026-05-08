## Knowledge about linux
### initramfs
- Initial RAM filesystem is a temporary filesystem image used to help the linux kernel mount the root filesystem and run the main init system.
- initramfs is initialized at boot time. 
    - Kernel checks for the presence of the initramfs and, if found, mounts it as / and runs /init. 

#### INSecurities
- initramfs is a high-value target because it runs before the main operating system is fully loaded and often lacks the cryptographic signatures required by secure boot. 
    - Bypass Full-Disk Encryption
    - Persistent Malware Injection
    - Gain a root Debug Shell
    - Exfiltrate Data
    - Backdoor the "init" process
##### Common Vulnerabilitites
- CVE-2016-4484
    - A well-known flaw where holding the enter key for ~70 seconds at the LUKS password prompt drops the user into a root shell.

[Link](https://www.linuxfromscratch.org/blfs/view/svn/postlfs/initramfs.html)


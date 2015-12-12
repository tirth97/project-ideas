# project-ideas

## Operating system


    + Build a virtual machine monitor that can run multiple guests (for example, multiple instances of JOS), using x86 VM support.
    + Do something useful with the x86 Trusted Execution Technology. For example, run applications without having to trust the kernel. This resource may not render correctly in a screen reader.Here (PDF) is a recent paper on this topic.
    + Fix xv6 logging to support concurrent transactions, and generally have higher performance, perhaps taking ideas from Linux EXT3.
    Use file system ideas from This resource may not render correctly in a screen reader.Soft updates (PDF), WAFL, ZFS, or another advanced file system.
    Add snapshots to a file system, so that a user can look at the file system as it appeared at various points in the past. You'll probably want to use some kind of copy-on-write for disk storage to keep space consumption down.
    Implement This resource may not render correctly in a screen reader.capabilities (PDF) to provide fine-grained control over what privileges processes have.
    Build a This resource may not render correctly in a screen reader.distributed shared memory (PDF) (DSM) system, so that you can run multi-threaded shared memory parallel programs on a cluster of machines, using paging to give the appearance of real shared memory. When a thread tries to access a page that's on another machine, the page fault will give the DSM system a chance to fetch the page over the network from whatever machine currently stores.
    Layer software This resource may not render correctly in a screen reader.RAID-5 (PDF) over an array of disks, to increase fault tolerance and performance.
    Allow processes to migrate from one machine to another over the network. You'll need to do something about the various pieces of a process's state, such as file descriptors in xv6.
    Implement paging to disk in xv6 or JOS, so that processes can be bigger than RAM. Extend your pager with swapping.
    Implement mmap() of files for JOS or xv6.
    Implement loadable kernel modules to extend the xv6 kernel to replace or extend subsystems of the xv6 kernel. For example, make the file system a kernel module so that you can add a kernel module to read DOS file systems, or replace the xv6 file system.
    Use xfi to sandbox code within a process.
    Support x86 2MB or 4MB pages.
    Modify xv6 to have kernel-supported threads inside processes. See in-class uthread assignment to get started. Implementing scheduler activations would be one way to do this project.
    Implement ideas from the Exokernel papers, for example the packet filter.
    Make JOS or xv6 have soft real-time behavior. You will have to identify some application for which this is useful.
    Make JOS or xv6 run on 64-bit CPUs. This includes redoing the virtual memory system to use 4–level pages tables. See reference page for some documentation.
    Port JOS or xv6 to a different microprocessor. The osdev wiki may be helpful.
    A window system for xv6 or JOS, including graphics driver and mouse. See reference page for some documentation. sqrt(x) is an example JOS window system (and writeup).
    Implement This resource may not render correctly in a screen reader.dune (PDF) to export privileged hardware instructions to user-space applications in JOS or xv6.
    The linux kernel uses read copy update to be able to perform read operations without holding locks. Explore RCU by implementing it in xv6 and use it to support a name cache with lock-free reads
    Intel recently announced for its upcoming processors. Implement support for Intel's Transactional Synchronization Extensions in the QEMU emulator. A follow-on project would be to explore the use of Intel TSX primitives in writing concurrent software, such as extending a small multi-core operating system (based on 6.828's xv6) to use transactional memory.

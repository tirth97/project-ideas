# project-ideas

## Operating system


<ul>
    <li>Build a virtual machine monitor that can run multiple guests (for example, multiple instances of JOS), using x86 VM support.</li>
    <li>Do something useful with the x86 Trusted Execution Technology. For example, run applications without having to trust the kernel. <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://www.usenix.org/system/files/conference/osdi12/osdi12-final-51.pdf">Here (PDF)</a> is a recent paper on this topic.</li>
    <li>Fix xv6 logging to support concurrent transactions, and generally have higher performance, perhaps taking ideas from Linux EXT3.</li>
    <li>Use file system ideas from <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://www.ece.cmu.edu/~ganger/papers/osdi94.pdf">Soft updates (PDF)</a>, WAFL, ZFS, or another advanced file system.</li>
    <li>Add snapshots to a file system, so that a user can look at the file system as it appeared at various points in the past. You'll probably want to use some kind of copy-on-write for disk storage to keep space consumption down.</li>
    <li>Implement <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://pdos.csail.mit.edu/6.828/2012/readings/mazieres-hotos6.pdf">capabilities (PDF)</a> to provide fine-grained control over what privileges processes have.</li>
    <li>Build a <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://www.cdf.toronto.edu/~csc469h/fall/handouts/nitzberg91.pdf">distributed shared memory (PDF)</a> (DSM) system, so that you can run multi-threaded shared memory parallel programs on a cluster of machines, using paging to give the appearance of real shared memory. When a thread tries to access a page that's on another machine, the page fault will give the DSM system a chance to fetch the page over the network from whatever machine currently stores.</li>
    <li>Layer software <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://www.cs.cmu.edu/~garth/RAIDpaper/Patterson88.pdf">RAID-5 (PDF)</a> over an array of disks, to increase fault tolerance and performance.</li>
    <li>Allow processes to migrate from one machine to another over the network. You'll need to do something about the various pieces of a process's state, such as file descriptors in xv6.</li>
    <li>Implement paging to disk in xv6 or JOS, so that processes can be bigger than RAM. Extend your pager with swapping.</li>
    <li>Implement mmap() of files for JOS or xv6.</li>
    <li>Implement loadable kernel modules to extend the xv6 kernel to replace or extend subsystems of the xv6 kernel. For example, make the file system a kernel module so that you can add a kernel module to read DOS file systems, or replace the xv6 file system.</li>
    <li>Use <a href="http://static.usenix.org/event/osdi06/tech/erlingsson.html">xfi</a> to sandbox code within a process.</li>
    <li>Support x86 2MB or 4MB pages.</li>
    <li>Modify xv6 to have kernel-supported threads inside processes. See in-class uthread assignment to get started. Implementing scheduler activations would be one way to do this project.</li>
    <li>Implement ideas from the Exokernel papers, for example the packet filter.</li>
    <li>Make JOS or xv6 have soft real-time behavior. You will have to identify some application for which this is useful.</li>
    <li>Make JOS or xv6 run on 64-bit CPUs. This includes redoing the virtual memory system to use 4–level pages tables. See reference page for some documentation.</li>
    <li>Port JOS or xv6 to a different microprocessor. The <a href="http://wiki.osdev.org/Main_Page">osdev wiki</a> may be helpful.</li>
    <li>A window system for xv6 or JOS, including graphics driver and mouse. See reference page for some documentation. <a href="http://web.mit.edu/amdragon/www/pubs/sqrtx-6.828.html">sqrt(x)</a> is an example JOS window system (and writeup).</li>
    <li>Implement <img src="/images/inacessible.gif" alt="This resource may not render correctly in a screen reader."><a href="http://www.usenix.org/system/files/conference/osdi12/osdi12-final-117.pdf">dune (PDF)</a> to export privileged hardware instructions to user-space applications in JOS or xv6.</li>
    <li>The linux kernel uses read copy update to be able to perform read operations without holding locks. Explore RCU by implementing it in xv6 and use it to support a name cache with lock-free reads</li>
    <li>Intel recently announced for its upcoming processors. Implement support for Intel's Transactional Synchronization Extensions in the QEMU emulator. A follow-on project would be to explore the use of Intel TSX primitives in writing concurrent software, such as extending a small multi-core operating system (based on 6.828's xv6) to use transactional memory.</li>
    <li>Development of Syntax analyzer using Java.</li>
</ul>



<sub>Many of the ideas are taken from course projects of different universities such MIT,Nirma etc.</etc>

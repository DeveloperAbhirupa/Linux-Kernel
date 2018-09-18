# Linux-Kernel
AIM: To design a Linux kernel and implement memory management techniques, interrupt handling and keyboard and mouse device drivers



THEORY:

A kernel is the core component of an operating system. Using interprocess communication and system calls, it acts as a bridge between applications and the data processing performed at the hardware level.When an operating system is loaded into memory, the kernel loads first and remains in memory until the operating system is shut down again. The kernel is responsible for low-level tasks such as disk management, task management and memory management.


The kernel is responsible for:

    • Process management for application execution 
    
    • Memory management, allocation and I/O 
    
    • Device management through the use of device drivers 
    
    • System call control, which is essential for the execution of kernel services
    

Linux Kernel Architecture

Because the Linux kernel is monolithic, it has the largest footprint and the most complexity over the other types of kernels. This was a design feature still carries some of the same design flaws that monolithic kernels are inherent to have. Linux kernel developers made kernel modules that could be loaded and unloaded at runtime, meaning you can add or remove features of your kernel on the fly. This can go beyond just adding hardware functionality to the kernel, by including modules that run server processes, like low level virtualization.


Kernel Module


A loadable kernel module (LKM) is a mechanism for adding code to, or removing code from, the Linux kernel at run time. They are ideal for device drivers, enabling the kernel to communicate with the hardware without it having to know how the hardware works. The alternative to LKMs would be to build the code for each and every driver into the Linux kernel.
Kernel modules run in kernel space and applications run in user space, as illustrated in Figure 2. Both kernel space and user space have their own unique memory address spaces that do not overlap. This approach ensures that applications running in user space have a consistent view of the hardware, regardless of the hardware platform. The kernel services are then made available to the user space in a controlled way through the use of system calls. The kernel also prevents individual user-space applications from conflicting with each other or from accessing restricted resources through the use of protection levels (e.g., superuser versus regular user permissions).

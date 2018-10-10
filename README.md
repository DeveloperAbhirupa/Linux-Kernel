# Linux-Kernel
AIM: To design a Linux kernel and implement memory management techniques, interrupt handling and keyboard and mouse device drivers



THEORY:

A kernel is the core component of an operating system. Using interprocess communication and system calls, it acts as a bridge between applications and the data processing performed at the hardware level.When an operating system is loaded into memory, the kernel loads first and remains in memory until the operating system is shut down again. The kernel is responsible for low-level tasks such as disk management, task management and memory management.


start.asm
---------

It is the kernel's entry point. It will be executed FIRST when the bootloader invokes the kernel. This file loads a new 8KByte stack, and then jump into an infinite loop. The stack is a small amount of memory, but it's used to store or pass arguments to functions in C. It's also used to hold local variables that we declare and use inside our functions. Any other global variables are stored in the data and BSS sections. The lines between the 'mboot' and 'stublet' blocks make up a special signature that GRUB uses to verify that the output binary that it's going to load is, infact, a kernel.

linker.ld
---------
It takes all of our compiler and assembler output files and links them together into one binary file.
'Text' or 'Code' is the executable itself. The 'Data' section is for hardcoded values in your code, such as when you declare a variable and set it to 5. The value of 5 would get stored in the 'Data' section. The last section is called the 'BSS' section. The 'BSS' consists of uninitialized data; it stores any arrays that you have not set any values to.

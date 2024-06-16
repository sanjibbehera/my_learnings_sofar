## What is Linux OS?
**Linux®** is an open source operating system (OS). An operating system is the software that directly manages a system’s hardware and resources, like CPU, memory, and storage. The OS sits between applications and hardware and makes the connections between all of your software and the physical resources that do the work.

## How does Linux work?
Linux was designed to be similar to UNIX, but has evolved to run on a wide variety of hardware from phones to supercomputers. Every Linux-based OS involves the Linux kernel—which manages hardware resources—and a set of software packages that make up the rest of the operating system.  
The OS includes some common core components, like the GNU tools, among others. These tools give the user a way to manage the resources provided by the kernel, install additional software, configure performance and security settings, and more. All of these tools bundled together make up the functional operating system. Because Linux is an open source OS, combinations of software can vary between Linux distributions.

## What is the Linux kernel?
The Linux® kernel is the main component of a Linux operating system (OS) and is the core interface between a computer’s hardware and its processes. It communicates between the 2, managing resources as efficiently as possible.  
The kernel has 4 jobs:
- **Memory management**: Keep track of how much memory is used to store what, and where
- **Process management**: Determine which processes can use the central processing unit (CPU), when, and for how long
- **Device drivers**: Act as mediator/interpreter between the hardware and processes
- **System calls and security**: Receive requests for service from the processes

The kernel, if implemented properly, is invisible to the user, working in its own little world known as kernel space, where it allocates memory and keeps track of where everything is stored. What the user sees—like web browsers and files—are known as the user space. These applications interact with the kernel through a system call interface (SCI).

## Where the kernel fits within the OS?
To put the kernel in context, you can think of a Linux machine as having 3 layers:
- **The hardware**: The physical machine—the bottom or base of the system, made up of memory (RAM) and the processor or central processing unit (CPU), as well as input/output (I/O) devices such as storage, networking, and graphics. The CPU performs computations and reads from, and writes to, memory.
- **The Linux kernel**: The core of the OS. (See? It’s right in the middle.) It’s software residing in memory that tells the CPU what to do.
- **User processes**: These are the running programs that the kernel manages. User processes are what collectively make up user space. User processes are also known as just processes. The kernel also allows these processes and servers to communicate with each other (known as inter-process communication, or IPC).

## Linux OS Boot process
![Linux OS Booting Process](Images/LinuxOSBootupProcess.webp)

- Step 1 - When we turn on the power, BIOS (Basic Input/Output System) or UEFI (Unified Extensible Firmware Interface) firmware is loaded from non-volatile memory, and executes POST (Power On Self Test)
- Step 2 - BIOS/UEFI detects the devices connected to the system, including CPU, RAM, and storage.
- Step 3 - Choose a booting device to boot the OS from. This can be the hard drive, the network server, or CD ROM.
- Step 4 - BIOS/UEFI runs the boot loader (GRUB), which provides a menu to choose the OS or the kernel functions.
- Step 5 - After the kernel is ready, we now switch to the user space. The kernel starts up systemd as the first user-space process, which manages the processes and services, probes all remaining hardware, mounts filesystems, and runs a desktop environment.
- Step 6 - systemd activates the default. target unit by default when the system boots. Other analysis units are executed as well.
- Step 7 - The system runs a set of startup scripts and configure the environment.
- Step 8 - The users are presented with a login window. The system is now ready.
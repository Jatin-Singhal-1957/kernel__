Operating System Kernel
This project is an operating system kernel written in C and assembly language. It includes components such as a bootloader, paging system, heap manager, interrupt descriptor table (IDT), and VGA text mode output.

Project Structure
Bootloader: bootloader.asm

A 16-bit assembly bootloader that sets up the system and jumps to the kernel.
Kernel: kernel.c

The main kernel code that initializes VGA text mode, handles memory management, and sets up paging.
Header Files:

kernel.h: Declarations for kernel functions.
heap.h: Definitions and declarations for heap management.
kheap.h: Declarations for kernel heap management.
idt.h: Definitions and declarations for the interrupt descriptor table.
paging.h: Declarations and definitions for the paging system.
Heap Management:

heap.c: Implements a basic heap manager with functions for creating heaps, allocating, and freeing memory blocks.
kheap.c: Implements kernel heap management, including functions for initializing the kernel heap and allocating memory.
Interrupt Descriptor Table (IDT):

idt.c: Sets up and initializes the IDT, including handling basic interrupts.
Paging:

paging.c: Implements paging, including directory and table management, and provides functions for setting up paging and switching directories.
Building and Running
Assemble and Link the Bootloader and Kernel:

Assemble the bootloader with an assembler like NASM: nasm -f bin bootloader.asm -o bootloader.bin
Compile and link the kernel with a cross-compiler like GCC.
Create a Bootable Image:

Combine the bootloader and kernel into a bootable disk image using a tool like dd or cat.
Run in an Emulator:

Use an emulator like QEMU to test the kernel: qemu-system-x86_64 -drive format=raw,file=bootable_image.img
Functions and Components
Kernel Main (kernel_main): Initializes the VGA text mode, prints a message, sets up heap management, initializes the IDT, and sets up paging.

Heap Functions:

heap_create(): Initializes a new heap.
heap_malloc(): Allocates memory from the heap.
heap_free(): Frees memory back to the heap.
IDT Functions:

idt_init(): Initializes the IDT and loads it into memory.
idt_set(): Sets an interrupt descriptor in the IDT.
Paging Functions:

paging_new_4gb(): Creates a new 4GB paging chunk.
paging_switch(): Switches to a new page directory.
paging_set(): Sets up paging for a specific virtual address.
# Project Completion

This project is now complete. Thank you for your interest and support!

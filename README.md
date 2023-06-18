# Linux Kernel Module - Process DFS Traversal

This Linux kernel module provides a functionality to traverse and list all processes in Depth-First Search (DFS) order. It displays information such as process name, PID, and state for each process encountered during the traversal.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Building](#building)
- [Installation](#installation)
- [Author](#author)

## Introduction

The process DFS traversal module is designed to run within the Linux kernel and provides a method to list all processes in DFS order. The DFS algorithm starts from the root task and recursively visits child processes until all processes have been traversed. This can be useful for understanding the process hierarchy and obtaining information about running processes.

## Usage

To use this module, you need to have a Linux system with a working kernel build environment. Follow these steps:

1. Clone or download this repository to your local machine.

2. Open a terminal and navigate to the repository directory.

 ![1](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/942e49ec-06a9-4a6d-bc2c-877cc999c747)

3. Build the kernel module by running the following command:

make

![2](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/60405f90-48c5-4e0b-b0e1-7d38de6190f6)

4. Load the module into the kernel using the following command:

sudo insmod main.ko

![3](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/a0a3af60-b7a0-4c40-8027-85e055f3706a)

5. You can check whether the module is loaded or not using:

lsmod 

![4](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/43884622-044c-4576-bec1-b50defd1328a)

6. You can check the module info using:

sudo modinfo main.ko

![5](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/652e1f69-eba8-4f3c-8671-3f0d7e691eed)

7. Check the kernel log to see the DFS traversal of the process tree:

dmesg

![6](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/87782076-620f-400a-afce-27148991a634)

8. After you have finished, unload the module from the kernel:

sudo rmmod main

![7](https://github.com/Darsh1907/Kernel-Developement/assets/118650412/3d8bcfd5-a73f-4842-a039-ec793e5499c3)


## Building

Before building the kernel module, ensure that you have a working kernel build environment on your Linux system. Additionally, make sure you have the necessary kernel headers installed.

The provided Makefile simplifies the build process. Open a terminal and navigate to the module directory. Run the following command to build the module:

make

This command will compile the module using the kernel build system. The resulting object file (`main.o`) will be generated in the same directory.

## Installation

To install the kernel module, follow the usage instructions mentioned above. Make sure to load and unload the module using `insmod` and `rmmod` commands with appropriate privileges (e.g., using `sudo`).

## Author

This Linux kernel module was developed by Darsh Patel (https://github.com/Darsh1907). If you have any questions or suggestions, please feel free to contact me.


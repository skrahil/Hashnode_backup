---
title: "Linux  Architecture | What are the basic Linux Commads | What is the difference between Update and Upgrade ?"
datePublished: Sun Jul 16 2023 19:39:34 GMT+0000 (Coordinated Universal Time)
cuid: clk5uc1ne000709lbfz7b5rxm
slug: linux-architecture-what-are-the-basic-linux-commads-what-is-the-difference-between-update-and-upgrade
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689532371926/46fff5db-2d7b-495d-881f-ea2f5bd2c2a6.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1689536345971/a4e42284-252e-4557-80ba-69634ae2bdc0.jpeg
tags: devops, devops-journey, trainwithshubham, tws, devopscommunity

---

# What is Linux?

Linux is an open-source operating system kernel that serves as the foundation for various Unix-like operating systems. It was initially developed by Linus Torvalds in 1991 and has since become one of the most widely used operating systems worldwide.

## Why Linux OS is so Famous?

* It's open-source nature. This means that its source code is freely available to the public, allowing developers to study, modify, and distribute it as per their requirements.
    
* Linux supports a wide range of software applications and services, including web servers, databases, programming languages, office suites, multimedia tools, and more
    
* The Linux community is vast and vibrant. Users can seek help, share knowledge, and collaborate with fellow enthusiasts, making problem-solving and learning easier.
    
* Linux is typically free to use and distribute. It reduces licensing costs and allows organizations and individuals to allocate their resources more efficiently.
    
* Linux has a robust security framework. Its open-source nature facilitates rapid identification and resolution of security vulnerabilities.
    

## Linux Architecture

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689533811066/ab962872-5874-4b9a-9ec1-42b4565021b6.png align="center")

> The Linux architecture is largely composed of elements such as the Kernel, System Library, Hardware layer, System, and Shell functions.

**Hardware layer:** The hardware layer of Linux is made up of several peripheral devices such as a CPU, HDD, and RAM

**Kernel:** The kernel is one of the fundamental parts of an operating system. It is responsible for each of the primary duties of the Linux OS. Each of the major procedures of Linux is coordinated with hardware directly. The kernel is in charge of creating an appropriate abstraction for concealing trivial hardware or application strategies. The following kernel varieties are mentioned:

1. Monolithic Kernel 
    
2. Micro kernels 
    
3. Exo kernels 
    
4. Hybrid kernels
    

**System Libraries:** A set of library functions may be specified as these functions. These functions are implemented by the operating system and do not require code access rights on the kernel modules.

**System Utility Programs:** A system utility program performs specific and individual jobs.

**Shell:** Different operating systems are classified as graphical shells and command-line shells. A graphical shell is an interface between the kernel and the user. It provides kernel services, and it runs kernel operations.

## Basic Linux Commands

* Listing of files: ls
    
* Changing Directory: cd
    
* Creating files: touch "filename"
    
* Copying files: cp Source Destination
    
* Removing files: rm filename
    
* Adding User: sudo useradd name
    
* Removing: Userdel -r username
    
* Checking Present Directory: pwd
    
* Displaying the content of files: cat
    

Output

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689535818064/8e462256-0703-403e-b077-057ed080afb6.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689535889552/e559b453-a2bb-4172-9d80-e7f57d71c275.png align="center")

## What is the difference between Update and Upgrade?

The update command only gets the information about the latest version of packages available for your system. It doesn’t download or install any package. It is the apt upgrade command that actually downloads and upgrades the package to the new version.

> HAPPY LEARNING
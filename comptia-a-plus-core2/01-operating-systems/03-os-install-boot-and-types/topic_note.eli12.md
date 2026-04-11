An operating system is like the main brain of your computer. Before you can play a video game, type a homework assignment, or watch a video, the operating system has to be installed and working perfectly with all the computer parts. If you are the person fixing the computers, you get to decide how to set up this brain. 

Fixing one computer for a friend is very different from setting up hundreds of computers for a whole school. 

Let's say you have to figure out how many computers you are setting up for a school project. 
1. First, you count the number of classrooms: there are 5 classrooms. 
2. Next, you count the computers needed for each classroom: there are 20 computers. 
3. Finally, you multiply those numbers together: 5 * 20 = 100 total computers. 

Fixing one computer is easy, but setting up 100 means you need a smarter plan! Learning how to start up the computer and how to install its main software is super important. 

## The Ignition Sequence: Boot Methods

Before you can install an operating system, you have to tell the computer where to find the setup files. A brand-new computer has a totally blank memory. You have to introduce the setup files to the system so it knows what to do.

To do this, we use something called an ISO file. An ISO file is a sector-by-sector disk image used to create bootable installation media. Think of an ISO file as a perfect digital mold—it has the exact copy of every single file the computer needs to wake up and start working!

### Physical Boot Media

A long time ago, people used discs to start up computers. Optical media formats like CDs and DVDs serve as legacy boot methods for operating system installation. "Legacy" just means it is an older way of doing things. 

Today, we use something much smaller and faster. A USB flash drive provides a portable medium for storing an operating system installation image. You can buy one at the store for about \$15 or \$20. But just plugging it in isn't enough! Installing an operating system from a USB flash drive requires configuring the system BIOS or UEFI to boot from a USB device. The BIOS or UEFI is a tiny menu built into the computer. You have to go into that menu and tell the computer to look at the USB drive first, instead of its own empty hard drive.

If you want things to go even faster, you can use a solid-state drive (SSD). An external solid-state drive can serve as a high-speed bootable installation medium via a USB connection. It is just like a USB flash drive, but way faster! Also, solid-state drives can be partitioned to hold a bootable installation image alongside normal storage data. "Partitioned" means dividing the drive into different rooms. One room can hold the setup files, and the other room can hold your personal pictures and games. 

### Recovery Partitions

Sometimes, the setup files are already hiding inside the computer! A recovery partition is a hidden section of a hard drive created by the original equipment manufacturer. This means the company that built the computer (like HP or Dell) put a secret room on the hard drive. 

A recovery partition contains a factory-state image used to reinstall the operating system without external media. If your computer breaks while you are on vacation and you don't have a USB drive, you can just press a special button to use this hidden partition. It will wipe the computer and make it exactly like it was on the day it was bought from the store.

### Network Booting (PXE)

What if you have to set up 50 computers, but you don't want to plug a USB drive into every single one? You can use the internet cables! 

PXE stands for Preboot Execution Environment. A PXE boot enables a computer to boot using a network interface instead of a local storage drive. This means the computer turns on and shouts across the network cable, "Hey! Can someone send me the setup files?"

For this to work, two special helpers on the network must answer:
1. PXE booting requires a DHCP server to provide an IP address to the booting client. The computer needs a network address so the server knows exactly where to send the files.
2. PXE booting requires a TFTP server to deliver the initial boot files over the network. Think of TFTP like the mail carrier bringing the first package of setup instructions.

## Evaluating the Terrain: Installation Types

Once the computer finds the setup files, you have to choose *how* you want to install them. Your choice decides if the user's saved games and pictures get erased or kept.

### The Clean Install

A clean installation formats the target storage volume before installing the operating system. This means it completely wipes the drive totally clean, like erasing a chalkboard. 

Because it wipes everything, a clean installation completely deletes all existing user data on the target storage volume. It also completely deletes all previously installed applications on the target storage volume. You only do this when the computer has a really bad virus, or if you are giving your old computer to a totally new person. 

### The In-Place Upgrade

When a new version of Windows comes out, you usually don't want to delete all your stuff just to get the new version. An in-place upgrade replaces an existing operating system with a newer version. 

This is the best way to upgrade because an in-place upgrade preserves user files during the operating system installation process. Also, an in-place upgrade preserves installed applications during the operating system installation process. Finally, an in-place upgrade preserves system configuration settings during the operating system installation process. Your desktop wallpaper, your saved games, and your favorite apps stay exactly where you left them!

### The Repair Installation

Sometimes a computer starts crashing, but you really don't want to lose your files. A repair installation fixes a corrupted operating system by replacing system files without deleting user data. It is like a mechanic fixing a broken car engine without taking any of your CDs or sunglasses out of the front seat. 

### Multiboot Installations

Some computer experts want to play games on Windows but also practice coding on Linux using the exact same computer. A multiboot installation allows a single computer to host multiple operating systems. 

To make this work, there are two strict rules:
1. A multiboot installation requires each operating system to be installed on a separate logical partition or physical drive. They have to live in separate rooms so they don't mess up each other's files.
2. A multiboot setup requires a boot manager to present an operating system selection menu at computer startup. When you turn on the computer, the boot manager pops up on the screen and asks, "Which system do you want to use today?"

## The Enterprise Scale: Deployment Methodologies

If you are setting up one computer, clicking "Next" on the screen is fine. But if you are setting up hundreds of computers for a big business, clicking "Next" hundreds of times would take forever! We have to use automation, which is like using a robot to do the chores.

### Unattended Installations

An unattended installation automates the setup process by reading configuration details from a predefined file. Instead of a human sitting there to type in the time zone, a file does it automatically. 

For Microsoft computers, Windows unattended installations typically use an XML answer file named autounattend.xml. Think of this like a cheat sheet for the computer. An answer file provides pre-configured responses for setup prompts like time zone, language, and computer name. The computer reads the file and installs everything by itself!

### Image Deployment and Sysprep

Big businesses want every single computer to look exactly the same. Image deployment involves applying a captured operating system image onto a target computer drive. It’s like taking a perfect photograph of one awesome computer setup, and stamping that exact same setup onto every other computer. Image deployment standardizes operating system configurations across multiple enterprise computers. 

But there is a catch! If you perfectly copy a computer, you also copy its secret network ID badge. To fix this, the Windows Sysprep utility removes hardware-specific information from an operating system before image capture. Removing device-specific information with Sysprep prevents security identifier conflicts on an enterprise network. It basically erases the ID badge from the "photograph" so every new computer can get its very own unique badge when it turns on.

### Remote and Automated Deployments

If you are in charge of computers in entirely different buildings, you can set them up without ever leaving your chair. Remote network installation allows IT administrators to deploy operating systems to endpoint devices located in different physical facilities. Remote network installations frequently utilize tools like Windows Deployment Services to serve installation images over a local area network.

There are two main ways to do this over the network:

**Lite-Touch Deployment**
Lite-touch deployment is an automated installation method requiring minimal manual input at the target device. It does almost everything by itself, but lite-touch deployment often requires a technician to manually initiate the network boot sequence on the endpoint. You just have to walk over, press a button like F12 to start the PXE network boot, and the computer takes over the rest.

**Zero-Touch Deployment**
This is the ultimate magic trick. Zero-touch deployment installs an operating system over the network without any physical interaction at the target computer. You don't even have to touch the keyboard! Zero-touch deployment is suited for deploying standardized operating systems to thousands of enterprise endpoints simultaneously. 

However, this doesn't happen by accident. Zero-touch deployment requires comprehensive server infrastructure configuration to automate the entire imaging process. You have to build a very smart, complex network of servers behind the scenes so the computers know exactly how to set themselves up the second they get plugged into the wall.
---
layout: post
title: "Blog 10"
---
How to Create a Disk Partition in Linux
---------------------------------------

How to partition a disk using the "parted" command.

The first step is to view the partition table or layout on all block devices. This helps you identify the storage device you want to partition. The -l flag means list partition layout on all block devices.

	$ sudo parted -l
	(Will prompt for password)

Results:

	Model: ATA VBOX HARDDISK (scsi)
	Disk /dev/sda: 21.5GB
	Sector size (logical/physical): 512B/512B
	Partition Table: msdos
	Disk Flags:

	Number  Start   End     Size    Type     File system  Flags
	1      1049kB  21.5GB  21.5GB  primary  ext4         boot

From the output of the above command, there is one hard disk attached to the system, which is /dev/sda.

To manipulate disk partitions, open the hard disk to start working on it, as shown.

	$ sudo parted /dev/sda

Results:

	GNU Parted 3.2
	Using /dev/sda
	Welcome to GNU Parted! Type 'help' to view a list of commands.

At the parted prompt, make a partition table by running mklabel, msdos, or gpt, then enter Y/es to accept it.

	(parted) mklabel msdos
	Warning: Partition(s) on /dev/sda are being used.

You will asked to ignore the warning or cancel

	Ignore/Cancel? ignore                                                	 
	Warning: The existing disk label on /dev/sda will be destroyed and all data on this disk will be lost. Do you want to continue?

Y or Yes to continue

	Yes/No? yes

An error message will occur, just ignore it

	Error: Partition(s) 1 on /dev/sda have been written, but we have been unable to inform the kernel of the change, probably because it/they are in use.  As a	result, the old partition(s) will remain in use.  You should reboot now before	making further changes.

Next, make the partitions

	(parted) mkpart primary ext4 [enter size]
	(parted) mkpart primary ext4 [enter size]

To view created partitions, use

	(parted) print

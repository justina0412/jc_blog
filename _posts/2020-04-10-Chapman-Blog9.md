---
layout: post
title: "Blog 9"
---
How to Install PowerShell in Ubuntu
-----------------------------------

There are two ways to install PowerShell in Ubuntu i.e. via terminal or via Ubuntu Software Application.

### Using the Terminal

	1. Open the terminal
	2. Snap command to install PowerShell
		$ snap install powershell -classic
		(may need to use "--classic")
	3. PowerShell should now be installed. It should say 'installed' along with the version

	Note: Use sudo when using the command. The system may prompt you for authentication.

	4. To start PowerShell, run this command:
		$ powershell

### Using Ubuntu Software

	1. Open Ubuntu Software Manager
		This can be found in the Application Menu
	2. search: powershell
		There are 2 options:
		- powershell
		- powershell-preview

	Make sure to choose 'powershell'
	3. Click the 'install' button
	4. After installing, click the 'launch' button

#### Test if PowerShell is working

This can be done with a few commands.

	1. Open the PowerShell Terminal
	2. Enter the command:
		$PSVersionTable
		This will show the version of powershell installed.

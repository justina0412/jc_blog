---
layout: post
title: "Blog 11"
---
How to Install Node.js on Linux
-------------------------------

"Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine. Node.js can be installed in multiple ways on your Ubuntu Linux machine."How to

#### Step 1

Open the terminal (shortcut: Ctrl + Alt + T)

#### Step 2

Install using the following command:

	$ sudo apt install nodejs


#### Step 3

Verify installation & check version

	$ node -v
	OR
	$ node -version

**Note**: It is recommended to install Node Package Manager(NPM) with Node.js. NPM is an open source library of Node.js packages.

To install NPM, use the following commands:

	$ sudo apt install npm

	Enter "Y" to use disk space

	Check installation/version:

	$ npm -v or npm –version


## Install Node.js using NodeSouce Repository

#### Step 1

Open the terminal and update & upgrade the package manager

	$ sudo apt-get update
	$ sudo apt-get upgrade

#### Step 2

Install Python software libraries using the following command:

	$ sudo apt-get install python-software-properties

#### Step 3

Add Node.js PPA to the system

	$ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash –

#### Step 4

Install Node.js and NPM to your Ubuntu machine, use the command given below:

	$ sudo apt-get install nodejs

#### Step 5

Check installation/version:

	$ node -v
	OR
	$ node –version
	OR
	$ npm -v
	OR
	$ npm –version

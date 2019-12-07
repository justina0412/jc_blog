---
layout: post
title: "Blog 12"
---

How to install Ansible in Ubuntu
-------------------------------------------

Initially, I was going to continue blog 11, but I kept running into problems with installing Ansible. So here are the proper commands to install Ansible.

1. Update and upgrade Ubuntu

		$ sudo apt-get update
		$ sudo apt-get upgrade -y


2. Install the repository with Ansible

		$ sudo apt-add-repository ppa:ansible/ansible

3. update

		$ sudo apt-get update

4. Install ansible

		$ sudo apt-get install ansible -y

5. A Python interpreter is required to run modules. Install Python

		$ sudo apt-get install python -y

6. Check if Python was installed correctly

		$ python --version

7. Check if Ansible was installed correctly

		$ ansible --version

After going through the commands listed, the problem ended up being the terrible wifi at Starbucks. Ansible is now installed :)

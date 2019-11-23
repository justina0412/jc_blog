---
layout: post
title: "Blog 11"
---

The next few blogs will be going over ansible basics to help with the final project.


Ansible works by connecting to your nodes and puishing out modules. Ansible executes them over SSH, and then removes them. There are over 750 built in modules.

"Playbooks can finely orchestrate multiple slices of your infrastructure topology, with very detailed control over how many machines to tackle at a time...They can describe a policy you want your remote systems to enforce, or a set of steps in a general IT process." (ansible.com). Ansible provides plenty of documentation regarding playbooks. Documenation can be found here:

	https://docs.ansible.com/ansible/latest/user_guide/playbooks.html

Playbooks are written in YAML.YAML syntax can be found here:

  https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html#yaml-syntax

Playbook Basics
---------------
In a playbook, you get to choose which machine to target within the infrastructure and the remote user that will complete the 'tasks.'


The "hosts" line is a list of one or more groups or host patterns, separated by colons.

The remote_user is just the name of the user account.

Example:
	   - hosts: webservers
  	    remote_user: root

"remote_user" can be assigned for each task.

Example:
	 ---
	   - hosts: webservers
  	     remote_user: root
 	       tasks:
   	      - name: test connection
     	        ping:
              remote_user: yourname

"become" can be used on a certain task instead of a whole play

Example:
	---
	     - hosts: webservers
  	     remote_user: yourname
  	     tasks:
  	      - service:
      	        name: nginx
      	        state: started
     	      become: yes
            become_method: sudo

To be continued in Blog 12...

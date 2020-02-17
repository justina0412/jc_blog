---
layout: post
title: "Blog 3"
---

Installing Docker on Windows
-----------------------------

1. Install VirtualBox

2. Download docker-machine for creating Docker hosts

      cd c:\docker
      curl -L https://github.com/docker/machine/releases/download/v0.16.2/docker-machine-Windows-x86_64.exe --output docker-machine.exe

3. Install tinycorelinux as Docker host in VirtualBox

      docker-machine create --driver virtualbox --virtualbox-memory 4096 default

   After, check if it's working...

      docker-machine ssh

   To print the IP address...

      docker-machine ip

4. Download docker-client

      curl -L https://dockermsft.blob.core.windows.net/dockercontainer/docker-19-03-5.zip --output docker-19-03-5.zip

   Unzip the file into c:\docker and delete dockerd.exe

5. Create a batch file start_docker.bat in c:\docker

      docker-machine start
      docker-machine.exe env --shell cmd >c:\docker\setenv.bat
      call c:\docker\setenv.bat
      del c:\docker\setenv.bat

6. Add c:docker to the system path

   Open System Properties. From the command line, you can run this command: sysdm.cpl

   Open Advanced -> Environment Variables and add the directory to the Path variable.

7. Set up shared folders

      docker-machine stop
      "c:\Program Files\Oracle\VirtualBox\vboxmanage" sharedfolder add default --name "data"     --hostpath "c:\docker\data" --automount
      docker-machine start

   Create a folder in the vm and mount the shared folder.    

      docker-machine.exe ssh default "sudo mkdir -p /mnt/data"
      docker-machine.exe ssh default "sudo mount -t vboxsf data /mnt/data"

   Check the IP of the docker host

      docker-machine.exe ip

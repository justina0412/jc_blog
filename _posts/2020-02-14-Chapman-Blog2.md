---
layout: post
title: "Blog 2"
---

Network Interfaces
------------------

The most common method to find network interface details is using the ifconfig command:

	$ ifconfig -a

If ifconfig isn’t found, install net-tools using:

	$ sudo apt install net-tools

Try the command again.

When you type the command:

	$ip addr

The output is the network interfaces on the system. For example:

	1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
  2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:30:a5:34 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global dynamic noprefixroute enp0s3
       valid_lft 86119sec preferred_lft 86119sec
    inet6 fe80::6e44:3ae0:2137:8de0/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
  3: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default
    link/ether 02:42:1f:37:23:b5 brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever

The command to view the routing table is:

	$ip route show

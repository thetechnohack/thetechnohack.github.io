---
date: 2021-02-06 03:20:24
layout: post
title: Brutespray – Port Scanning and Automated Brute Forcing Tool
subtitle: Auto Brute Forcing Scanned Services 
description: BruteSpray is an open source python tool which provides a combination of both port scanning and automated brute force attacks against scanned services...
image: https://res.cloudinary.com/morphy/image/upload/v1612602917/brutespray/brutespray_zhqhak.png
optimized_image: https://res.cloudinary.com/morphy/image/upload/h_399,w_760,c_scale/v1612602917/brutespray/brutespray_zhqhak.png
category: tutorial
tags:
  - kali-linux
  - python
  - terminal
  - bruteforce
  - hacking
author: sumitpatidar
---

# Brutespray
BruteSpray is an open source python tool which provides a combination of both port scanning and automated brute force attacks against scanned services.

It takes the **GNMAP/XML** output from an Nmap scan and automatically brute forces the services running with default credentials using Medusa or use your dictionary to gain access.

# GitHub Stats
[![Status Card](https://github-readme-stats.vercel.app/api/pin/?username=x90skysn3k&repo=brutespray)](https://github.com/x90skysn3k/brutespray)


# Installing Brutespray
> Download the `.zip` file from GitHub and install it manually.

Or

> Run the following command to install `brutespray` package on Kali:

```bash
$ apt install brutespray
```

The following screenshot shows the output of the preceding command:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603125/brutespray/brutespray_installation_d3zpb7.png)

> Once it is installed, we can run the tool with the -h flag to view the list of all features and help.

```bash
$ brutespray -h
```

The following screenshot shows the output of the preceding help command:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603445/brutespray/brutespray_help_c4j0ey.jpg)

# How to do it...
We are doing this in 2 steps :
- Scanning Target

- Brute Forcing Targeted Services

## Scanning Target :
> First of all we need a target device.

> Here I'm using my own virtual machine as a target (IP: 192.168.1.5)

> So, let's scan this target using Nmap to find out which services are running.

```bash
$ nmap 192.168.1.5
```

In the following screenshot you can see running services on the targeted victims device:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603445/brutespray/nmap-services_xgqiw6.jpg)

> Now we need to save this Nmap output as an <ins>XML or GNMAP</ins> file.

> We are saving the Nmap output as an XML file on our desktop using the following command:

```bash
$ nmap 192.168.1.5 -oX /root/Desktop/scan.xml
```

You can see how this command looks alike:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603444/brutespray/nmap-scan_iu3vag.jpg)

> Now we can see that there is a file created on our desktop as **scan.xml**.

## Brute Forcing Targeted Services :

> To run a default brute force on all of the services that were discovered by a previously run Nmap scan, we can use the following command:

```bash
$ brutespray --file scan.xml --threads 5
```

The preceding command looks like this:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603222/brutespray/brutespray_command_e7xzts.png)

> To run the tool on one particular service, we can use the -s flag and
define the service we want to perform a brute force attack on. In the
following example, we will use the Nmap scan that was done on a host
and only check the default credentials on the FTP service:

```bash
$ brutespray --file scan.xml -t 5 -s ftp
```

The following screenshot shows the output of the preceding
command:

![image](https://res.cloudinary.com/morphy/image/upload/v1612603445/brutespray/scanning_ftp_mgmjkn.jpg)

> In the screenshot, we can see that the FTP allows anonymous
login, which is why the tool gave a success output for the credentials that
were shown.

> You can also use your custom user and password list to brute force.
For that you have to use -U and -P flag.

```bash
$ brutespray --file scan.xml -U username.txt -P passwords.txt -t 5 -s ftp
```

# Tutorial video
<iframe src="https://www.youtube.com/embed/C-CVLbSEe_g" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Practice and experiment about this tool on your own because the best ways to learn are practicing and experimenting. Take a deep dive and explore how this tool actually works.


| Drop your questions in the comment box ! |
| --- |

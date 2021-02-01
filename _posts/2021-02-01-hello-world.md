---
date: 2021-02-01 11:38:05
layout: post
title: How to install MySQL (MariaDB) on Android with Termux
subtitle: Easy installation of MariaDB-Cli on android using termux.
description: MariaDB is an open-source database management system, commonly used as an alternative for the MySQL in the LAMP (Linux, Apache, MySQL, PHP/Python/Perl) stack. It is intended to be a drop-in replacement for MySQL.
image: https://res.cloudinary.com/morphy/image/upload/v1612159107/termux-mariadb/mariadb-cli_q0zlcn.jpg
optimized_image: https://res.cloudinary.com/morphy/image/upload/v1612159107/termux-mariadb/mariadb-img_o9mksp.jpg
category: tutorial
tags:
  - sql
  - mysql
  - mariadb
author: sumitpatidar
---

## Introduction

Generally, smartphones are not for programming but with the rapid evolution of technology the capability of smartphone is also increasing. We can do many programming stuffs on smartphone using some applications.

In this blog, we are going to use a database management system in our smartphone using termux.

We cannot run Mysql effeciently on smartphone but alternatively we can use MariaDB as our database management system.
Mysql and mariadb have some similarities and differences.

MariaDB is an open-source database management system, commonly used as an alternative for the MySQL in the LAMP (Linux, Apache, MySQL, PHP/Python/Perl) stack. It is intended to be a drop-in replacement for MySQL.

This tutorial will explain how to install SQL(MariaDB) or MySQL command line Android.

It is a very beginner friendly guide with explanary images.

## Requirements

- termux app

- internet connection(for package installation)

#### *Install termux app*

![image](https://res.cloudinary.com/morphy/image/upload/v1612001129/termux-mariadb/termux-playstore_x1cy5h.jpg)

<button name="button"><a href="https://play.google.com/store/apps/details?id=com.termux">Download Termux</a></button>

<hr>

### Follow 4 easy steps:

## Step–1 Updating packages

- Open termux app.

- You can see a greeting screen like this:

![image](https://res.cloudinary.com/morphy/image/upload/v1612006811/termux-mariadb/termux-home_amfpn1.jpg)

- Type `apt update` command and press enter.

```bash
$ apt update
```

![image](https://res.cloudinary.com/morphy/image/upload/v1611993551/termux-mariadb/apt-update-image_vmelgi.jpg)

- Wait until the dollar sign appears again.

- Now type `apt upgrade` and press enter.

```bash
$ apt upgrade
```

![image](https://res.cloudinary.com/morphy/image/upload/v1611993552/termux-mariadb/apt-upgrade-image_zvjl8k.jpg)

- It will ask you for storage permission.

- Enter y and press enter.

![image](https://res.cloudinary.com/morphy/image/upload/v1611993551/termux-mariadb/termux-image_zdn7k7.jpg)

- If this message appears:

![image](https://res.cloudinary.com/morphy/image/upload/v1612088080/termux-mariadb/termux-image-skip_idtovk.jpg)

- Just press enter.

- Wait for a couple of minutes.

> Use `clear` command to clear screen.

<hr>

## Step–2 Installing MariaDB (MySQL)

- Type `pkg install mariadb` and press enter.

```bash
$ pkg install mariadb
```

![image](https://res.cloudinary.com/morphy/image/upload/v1612008282/termux-mariadb/install-mariadb_j0bps8.jpg)

-  It will again ask you for storage permission.

- Type y and press enter.

![image](https://res.cloudinary.com/morphy/image/upload/v1612008593/termux-mariadb/termux-image-2_qhkags.jpg)

- Wait until the process completes.

<hr>

## Step–3 Getting username (whoami)

- Type `whoami` command and press enter.

```bash
$ whoami
```
![image](https://res.cloudinary.com/morphy/image/upload/v1612009572/termux-mariadb/whoami-image-1_hrgiyh.jpg)

- It will give you a username.

- Copy or remember that username (or id).

![image](https://res.cloudinary.com/morphy/image/upload/v1612009572/termux-mariadb/whoami-image-2_t6xhdu.jpg)

## Step–4 Running and stoping MariaBD sessions

> You have to use this step every time you need to run MariaDB.

- Type the following command, just replace my username with yours.

```bash
$ mysqld_safe -u <username here>@localhost
```
![image](https://res.cloudinary.com/morphy/image/upload/v1612010517/termux-mariadb/mariadb-start-cmd_ntuuqo.jpg)

- Then your screen will look like this:

![image](https://res.cloudinary.com/morphy/image/upload/v1612011419/termux-mariadb/mariadb-start-cmd-2_gz3fhw.jpg)

- Press `ctrl+z` (alternatively you can open another session.)

![image](https://res.cloudinary.com/morphy/image/upload/v1612011395/termux-mariadb/mariadb-start-cmd-3_xp3iqs.jpg)

- Then type `mariadb` to start mariadb.

- Great! mariadb is running now.

![image](https://res.cloudinary.com/morphy/image/upload/v1612012273/termux-mariadb/mariadb-home_rigrwh.jpg)

- To exit mariadb, press `ctrl+z` or type exit

- After exiting MariaDB dont forget to kill the background session completely using the below command:

```bash
$ killall -u <Username here>
```

![image](https://res.cloudinary.com/morphy/image/upload/v1612012839/termux-mariadb/mariadb-kill_jphgix.jpg)

## Summary
- Update and upgrade packages using `apt update` & `apt upgrade`

- Install mariadb package using `pkg install mariadb`

- Start mariadb socket using `mysqld_safe -u <username>@localhost`

- Run mariadb using `mariadb` command

- Exit mariadb and then kill all background processes using `killall -u <username>`

## Conclusion
In this guide you installed MariaDB to act as an SQL server in android. Optionally, you also created a separate password-authenticated administrative user.

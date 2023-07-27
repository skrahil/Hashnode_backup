---
title: "Day 5 Task: Advanced Linux Shell Scripting for DevOps Engineers with User management"
datePublished: Thu Jul 20 2023 20:27:22 GMT+0000 (Coordinated Universal Time)
cuid: clkblsxj000010al41bsobyry
slug: day-5-task-advanced-linux-shell-scripting-for-devops-engineers-with-user-management
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689884767229/c82c71ab-f664-4826-a2da-a689205c1e44.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1689884831802/e74c1c5f-c625-43ce-b203-4dbaa55dc690.jpeg
tags: devops, 90daysofdevops, 90daysofdevopschallenge, tws, 90

---

## Write a bash script [createDirectories.sh](http://createDirectories.sh) that when the script is executed with three given arguments (one is directory name and second is start number of directories and third is the end number of directories ) it creates specified number of directories with a dynamic directory name

Script: Eval is the linux commad which is used to run the argument as a shell command⚙Here we are using three arguments 1st as a name of the directory 2nd as a start number 3rd as a end number.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689881591597/0927d04a-8295-4fc1-9bc9-a4b51d3af202.png align="center")

Output: Here we have to pass the argument while executing the script

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689881098701/0bec3a96-f7aa-4808-99e1-9d8b15e6aa8f.png align="center")

## Create a Script to back up all your work done till now.

Creating a Linux backup script is a great way to ensure your system’s data safety and integrity. Linux makes it easy to do so with bash, tar, rsync, and cron. Generally, you’ll want to start by writing a shell script that contains the specified Linux commands.

Script: First we have to give the Source and Destination path and i have used time stamped as a folder name for easy understanding the most important command is

```bash
tar -cpzf $destination $source
```

c: create

v: verbose mode, verbosely list files processed

p: preserve permissions for the new files

z: compress the files in order to reduce the size

f: use archive file or device ARCHIVE

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689881927187/62f0396b-aa7d-4874-87fb-7b49f7474609.png align="center")

Output:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689882058570/b0de1c50-e6d5-4788-a24e-b11ce2e90b3f.png align="center")

## Read About Cron and Crontab, to automate the backup Script

Corntab is a linux daemon that allows us to run scripts in certain scheduled moments. Crontab files automate backups, system maintenance and other useful tasks. In order to edit the crontab file with the editor you prefer(nano is the easiest), run in a terminal the command

```bash
crontab -e
#command to edit crontab
```

Let’s understand the contrab line format:

*minute(0–59) hour(0–23) day(1–31) month(1–12) weekday(0–6) command*

Let’s say that we want to run the script everyday at 12:30 a.m. we would type

```bash
29 0  * /bin/bash /path/backup_script.sh
#29 stands for the 30 minute
#0 stands for 12 a.m.
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689882222217/1073193d-245b-4209-854c-2d8c286c9e3b.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689882275636/6fa359bb-da6e-4c46-b0d4-10ab4951e500.png align="center")

## Create 2 users and just display their User names

To ADD User 👤

```bash
sudo useradd username
```

To DELETE User<sup>🔪</sup>

```bash
sudo userdell username
```

Using id command, you can get the ***ID of any username***. Every user has an id assigned to it and the user is identified with the help of this id. By default, this id is also the group id of the user. ✔

```bash
id username
```

To list out all USER in Linux

```bash
awk -F':' '{ print $1}' /etc/passwd
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689882821738/8903e8ce-a279-43ab-8334-44339b210834.png align="center")

So in this blog we have seen some advance shell scripting concepts, Automating tasks using Crontab,User management such Creating, Deletions of users🚠keep supporting guyzz if your have any queary feel free to ask.

## HAPPY LEARNING❤
---
title: "Day -3: Basic Linux Commands"
datePublished: Mon Jul 17 2023 17:44:38 GMT+0000 (Coordinated Universal Time)
cuid: clk75o3kw00010alc2mdrhlek
slug: day-3-basic-linux-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689614960768/f6cbaada-64d9-4474-9b76-1685137b1a53.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1689615816511/8ced13a7-db37-4ffa-a9d0-e9e6a2c8d654.jpeg
tags: devops, devops-articles, trainwithshubham, tws, shu

---

# Task: What is the linux command to:

# To view what's written in a file.

To view the contents of a file in Linux, you can use various command-line tools. The most common ones are `cat`, `less`, and `more`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613363684/ab68cc55-bda5-42b1-909c-02502893a7c9.png align="center")

## To change the access permissions of files.

In Linux, you can change the access permissions of files using the chmod command. The chmod command allows you to modify the read, write, and execute permissions for the owner, group, and other users.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613503340/8720c144-05d2-4177-bb71-35d87b61c106.png align="center")

## To check which commands you have run till now.

To check the commands you have run previously in Linux, you can make use of the command history. The history command allows you to view a list of previously executed commands in the current session. Here's how you can use it:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613567041/37bb492c-81b6-4ece-bce8-5b83de110b12.png align="center")

## To remove a directory/ Folder.

To remove a directory (or folder) in Linux, you can use the `rm` command with the `-r` option. The `-r` flag stands for "recursive" and is used to delete directories and their contents.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613748937/169bd31d-f9fe-4fa5-9aa4-24661554c817.png align="center")

## To create a fruits.txt file and to view the content.

To Create a file we can use various commands such touch, cat, vim, nano but touch is the most widely used command used to create files

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613890624/e995442c-2aaf-449b-8afa-7a4231e2a3e8.png align="center")

## Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava.

To add content to a file either we can use cat command or we can just use an editor such as vim,nano etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689613971163/f977c739-8f7c-453b-9215-39c2e567c9bb.png align="center")

## To Show only top three fruits from the file.

To Show only top three fruits from the file. To show only top three fruits we will use head command. The Linux head command prints the first lines of one or more files to standard output. By default, it shows the first 10 lines. We can pass a -n, where n show the specified number of line Syntax

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689614035783/a5b94a01-7299-4c87-b120-e982222006b8.png align="center")

## To Show only bottom three fruits from the file.

To Show only bottom three fruits from the file. To show only the bottom three fruits from the "devops.txt" file, you can use the "tail" command to display the last few lines of the file, like this: tail -n 3 devops.txt

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689614069457/f4bf3aeb-6874-498d-8023-2d44406efd63.png align="center")

## Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, Grey.

To add content to a file either we can use cat command or we can just use an editor such as vim,nano etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689614128406/5fa4c4b3-515e-4b8c-ae89-aff583a6d8e0.png align="center")

## To find the difference between fruits.txt and Colors.txt file.

To find the differences between two files in Linux, such as "fruits.txt" and "Colors.txt," you can use the `diff` command.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689614163119/93dfa7a4-3480-49f4-b13e-618415d98a47.png align="center")

> A Journey of Thousand miles begins with a single step
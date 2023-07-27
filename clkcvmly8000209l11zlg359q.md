---
title: "Day 6 Task: File Permissions and Access Control Lists🚀"
datePublished: Fri Jul 21 2023 17:50:09 GMT+0000 (Coordinated Universal Time)
cuid: clkcvmly8000209l11zlg359q
slug: day-6-task-file-permissions-and-access-control-lists
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689961756053/b1583fdb-5ecd-49cf-9114-61de2306a7c1.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1689961800348/a2e79b5e-3233-4ffe-9402-4cd5c1b2ef89.jpeg
tags: shell, 90daysofdevops, shubhamlondhe, 90daysofdevopschallenge, tws

---

## Create a simple file and do `ls -ltr` to see the details of the files.

Each of the three permissions are assigned to three defined categories of users. The categories are:

* ```bash
     owner   —   The owner of the file or  application.
    ```
    
* "chown" is used to change the ownership permission of a file or directory.
    
* ```bash
     group   —   The group that owns the file or application.
    ```
    
* "chgrp" is used to change the group permission of a file or directory.
    
* ```bash
     others  —   All users with access to the system. (outised the users are in a group)
    ```
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689958918456/799c45f0-261d-4650-9431-e6f50af7b41f.png align="center")

## File Permission in Linux

> ### **Check Permissions in Command-Line with Ls Command**

Go to the command line, you can easily find a file’s permission settings with the ls command, used to list information about files/directories. You can also add the –l option to the command to see the information in the long list format.  
To check the permission configuration of a file, use the command:

```bash
ls –l [file_name]
```

For instance, the command for the previously mentioned file would be:

```bash
ls –l test.txt
```

![using ls command to check permission with owner and group](https://phoenixnap.com/kb/wp-content/uploads/2021/04/using-ls-command-to-check-permission.jpg align="left")

As seen in the image above, the output provides the following information:

* file permission
    
* the owner (creator) of the file
    
* the group to which that owner belongs to
    
* the date of creation.
    

It shows the permission settings, grouped in a string of characters (-, r, w, x) classified into four sections:

1. **File type**. There are three possibilities for the type. It can either be a regular file (**–**), a directory (**d**) or a link (**i**).
    
2. **File permission of the user (owner)**
    
3. **File permission of the owner’s group**
    
4. **File permission of other users**
    

![file permission syntax explained](https://phoenixnap.com/kb/wp-content/uploads/2021/04/file-permission-syntax-explained.jpg align="left")

The characters **r**, **w**, and **x** stand for **read**, **write**, and **execute**.  
The categories can have all three privileges, just specific ones, or none at all (represented by  **–**, for denied).

Users that have **reading permission** can see the content of a file (or files in a directory). However, they cannot modify it nor add or remove. On the other hand, those who have **writing privileges** can edit (add and remove) files. Finally, being able to **execute** means the user can run the file. This option is mainly used for running scripts.

In the previous example, the output showed that test.txt is a regular file with read and write permission assigned to the owner, but gives read-only access to the group and others.

![permission settings for file output](https://phoenixnap.com/kb/wp-content/uploads/2021/04/permission-settings-for-file.jpg align="left")

## **Using Chmod Command to Change File Permissions** 

As all Linux users, you will at some point need to modify the permission settings of a file/directory. The command that executes such tasks is the `chmod` command.

The basic syntax is:

```bash
chmod [permission] [file_name]
```

There are two ways to define permission:

1. using **symbols** (alphanumerical characters)
    
2. using the **octal notation method**
    

### **Define File Permission with Symbolic Mode**

To specify permission settings using alphanumerical characters, you’ll need to define accessibility for the user/owner **(u)**, group **(g)**, and others **(o)**.

Type the initial letter for each class, followed by the equal sign **(=)** and the first letter of the read **(r)**, write **(w)** and/or execute **(x)** privileges.

To set a file, so it is public for reading, writing, and executing, the command is:

```bash
chmod u=rwx,g=rwx,o=rwx [file_name]
```

To set permission as in the previously mentioned **test.txt** to be:  
• read and write for the user  
• read for the members of the group  
• read for other users

Use the following command:

```bash
chmod u=rw,g=r,o=r test.txt
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689961529807/2bf23346-d7d5-4107-b70d-43a1e376db36.png align="center")

**Note**: There is no space between the categories; we only use commas to separate them.

Another way to specify permission is by using the octal/numeric format. This option is faster, as it requires less typing, although it is not as straightforward as the previous method.

Instead of letters, the octal format represents privileges with numbers:

* **r**ead has the value of **4**
    
* **w**(rite) has the value of **2**
    
* e**x**ecute has the value of **1**
    
* **no permission** has the value of **0**
    

The privileges are summed up and depicted by one number. Therefore, the possibilities are:

* **7 –** for read, write, and execute permission
    
* **6 –** for read and write privileges
    
* **5** – for read and execute privileges
    
* **4** – for read privileges
    

As you have to define permission for each category (user, group, owner), the command will include three (3) numbers (each representing the summation of privileges).

For instance, let’s look at the test.txt file that we symbolically configured with the `chmod u=rw,g=r,o=r test.txt`command.

The same permission settings can be defined using the octal format with the command:

```bash
chmod 644 test.txt
```

![chmod octal numeric format explained](https://phoenixnap.com/kb/wp-content/uploads/2021/04/chmod-octal-format-explained.jpg align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689961590416/145fe221-f3a9-423b-9468-8578671403db.png align="center")

## Access Control Lists Command (ACL )

Access Control List command provides an additional more flexible permission mechanism for file system. ACL is a Service which is used for providing special permission to specific user and group to a particular directory and files.

The two main ACL command are ⚙getfacl and setfacl🐱‍🏍

The `Getfacl` command is used to retrieve the ACLs of a file or directory. It shows the detailed ACL entries and their associated permissions for specific users and groups.

```bash
getfacl cron.txt
#first we need to install acl using: sudo apt install acl
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689960088265/1d82ac26-01a8-4f32-b872-29242a85d279.png align="center")

The `setfacl` command is used to set or modify ACLs on a file or directory. It allows you to define specific access permissions for individual users or groups.

```bash
setfacl -m g::rwx cron.txt
#Here we are adding read,write and execute permission to group and the file name is cron
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689960629902/4b421f31-fe77-4e58-903e-3811a6357ccd.png align="center")

## HAPPY LEARNING❤
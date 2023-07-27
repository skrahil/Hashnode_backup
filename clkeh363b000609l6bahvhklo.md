---
title: "DAY  8 : How to SSH? | User Management | Permission in Linux | Grep,Awk,Find| Systemctl"
datePublished: Sat Jul 22 2023 20:38:40 GMT+0000 (Coordinated Universal Time)
cuid: clkeh363b000609l6bahvhklo
slug: day-8-how-to-ssh-user-management-permission-in-linux-grepawkfind-systemctl
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690058027021/0e4b07a7-5a71-41aa-8d0d-0925141f0682.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1690103183129/f051fa63-dd54-4166-b70d-1e43a6f97d81.png
tags: devops, training, 90daysofdevops, trainwithshubham, 90daysofdevops-chanllenge

---

## User Management

User management in Linux is an essential aspect of system administration. It involves creating, modifying, and deleting user accounts, as well as managing user privileges and permissions. Here are some common user management tasks in Linux:

To Create a Group: To create a new group account, you can use the `groupadd` command.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690038511201/abf9c3de-c155-4736-b2c1-460679eb4d95.png align="center")

To view that group

```bash
sudo cat /etc/group
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690038676775/25cae573-767f-441c-ad90-b38af1dbf15a.png align="center")

To add a user to devops\_dev Group: To ad

```bash
sudo usermod -aG devops_dev user1
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690038867068/503a5453-be4c-481d-afef-059e36217534.png align="center")

To add multiple user to devops\_dev Group

```bash
sudo gpasswd -M user1,newuser tester
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690039013257/620d67ce-b7ec-4c1f-8461-55d312760204.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690039073777/9d82a747-0fe9-4611-b6fe-9dac559c071e.png align="center")

To Deleting a user account: If you need to remove a user account, you can use the `userdel` or gpasswd command:

```bash
sudo gpasswd -d user1 tester
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690039206562/7c86d734-58a3-4df6-8745-63574c2d2c28.png align="center")

## GREP (global regular expression print)

**A Unix command used to search files for the occurrence of a string of characters that matches a specified pattern.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690055450171/6f34e88f-8515-47ae-8993-2e6c1344ec5c.png align="center")

> \-i = case insensitive

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690055523129/bdcf1a89-6218-4b27-be92-bf8aa40aaf34.png align="center")

## awk

The `awk` command in Linux is a powerful text processing tool used for manipulating and extracting data from structured text files, typically in a columnar format. It takes its name from the initials of its creators: Alfred Aho, Peter Weinberger, and Brian Kernighan.

The basic syntax of the `awk` command is as follows:

```arduino
awk 'pattern { action }' file
```

The actual data is very confusing if we only want to display a selective column from that file we have to use "awk"

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690055748393/dd046205-8424-4d0a-8d3c-8a6352ea1d48.png align="center")

It will print "TRACE" and 3 coloumn

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690055839029/a5831d56-d048-4640-8325-6c2f060741a5.png align="center")

## find

The `find` command in Linux is a powerful utility that allows you to search for files and directories within a directory hierarchy based on various criteria. It is a versatile tool used from the command line. Here's the basic syntax of the `find` command:

```css
find [path] [expression]
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690055967539/a1ece09b-8004-42a2-ba65-a7f574105bfa.png align="center")

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

## SSH/SCP

SSH stands for Secure Shell, and it is a cryptographic network protocol used to securely access and manage remote systems in a Linux or Unix-like environment. It provides a secure way to establish a remote connection between two devices over an unsecured network, such as the internet. SSH encrypts the data transmitted between the client (your local machine) and the server (remote machine), preventing unauthorized access and eavesdropping.

## How can we connect out ec2instance to our local machine?📖📲

The most common way to connect to an EC2 instance is through SSH (Secure Shell). Below are the general steps to connect your EC2 instance to your local machine:

1. **Set up the EC2 instance:**
    
    * Launch an EC2 instance on AWS and note down its public IP address or public DNS name.
        
2. **Ensure the EC2 instance's security group allows SSH access:**
    
    * Make sure that the security group associated with your EC2 instance allows inbound SSH traffic (port 22) from your local machine's IP address. You can do this through the AWS Management Console.
        
3. **Local machine preparation:**
    
    * On your local machine, you will need an SSH client installed. Most Linux and macOS systems have an SSH client pre-installed. For Windows, you can use tools like PuTTY or the built-in Windows OpenSSH client.
        
4. **Connect via SSH:**
    
    * Open your terminal or command prompt on your local machine.
        
    * Use the following command to connect to your EC2 instance:
        
        ```vbnet
        ssh -i /path/to/your/private/key.pem ec2-user@your-instance-public-ip
        ```
        
        Replace `/path/to/your/private/key.pem` with the path to your private key file (.pem) that you used when launching the EC2 instance. Replace `your-instance-public-ip` with the public IP address or public DNS name of your EC2 instance.
        
5. **Logging in:**
    
    * If this is the first time connecting to the EC2 instance, you may be prompted to confirm the authenticity of the host. Type "yes" to continue.
        
    * You should now be logged into your EC2 instance through the SSH connection. You can execute commands on the EC2 instance directly from your local machine's terminal
        

## Systemctl:

Systemctl is a command-line tool used to control the systemd system and service manager in Linux distributions. It allows you to manage various aspects of system services, targets, and other units. Here are some commonly used systemctl commands:

1. Start a service:
    

```sql
sudo systemctl start service_name
```

1. Stop a service:
    

```arduino
sudo systemctl stop service_name
```

1. Restart a service:
    

```bash
sudo systemctl restart service_name
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1690057791989/d996b976-20f3-4c4e-b8d4-b140ba3bfae4.png align="center")

HAPPY LEARNING❤
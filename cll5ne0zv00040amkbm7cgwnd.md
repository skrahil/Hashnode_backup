---
title: "Day 9 Task: Deep Dive in Git & GitHub for DevOps Engineers."
datePublished: Thu Aug 10 2023 21:04:51 GMT+0000 (Coordinated Universal Time)
cuid: cll5ne0zv00040amkbm7cgwnd
slug: day-9-task-deep-dive-in-git-github-for-devops-engineers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1691701429521/292ddf6a-a7fb-40b4-909b-0f4afa3fed7a.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1691701470669/a430945c-7123-44f2-bc5c-d75606d921a0.png
tags: devops, 90daysofdevops, trainwithshubham, 90daysofdevops-devops-projectdevelopment-nonitbackground-github-docker-cloudplatforms-ec2-aws-elasticbeanstalk-lambdafunctions-devopspipelines-terraform-jenkins-docker-devsecops-scm-git-gitlab-bitbucket-buildtools-griddle-maven-ant-msbuild-monitoringtools-prometheus-grafana-ansible-ai-chatgpt-valueaddition-realworldproblems, 90daysofdevopschallenge

---

## 1\. What is Git and why is it important?

Git is a distributed version control system (DVCS) that is widely used for tracking changes in source code during software development. It was created by Linus Torvalds in 2005 and has become a fundamental tool in the field of software development.

### Git is important for several reasons:

1. **Version Control**: Git allows developers to track changes to their code over time. This is essential for collaborative projects, as multiple developers can work on the same codebase simultaneously, and Git helps manage and merge their changes seamlessly.
    
2. **Collaboration**: Git enables efficient collaboration among developers. It allows multiple individuals to work on different branches of a project and then merge their changes together. This prevents conflicts and ensures that changes are integrated smoothly.
    
3. **Branching and Merging**: Git's branching system allows developers to create separate branches for different features or bug fixes. This promotes parallel development and experimentation without affecting the main codebase. Merging branches back together is also made easier by Git.
    
4. **Backup and Recovery**: Git acts as a backup system, preserving every version of the codebase. If something goes wrong or a mistake is made, developers can revert to previous versions. This is particularly helpful for identifying and rectifying bugs.
    

# 2\. What is difference Between Main Branch and Master Branch??

The terms "Main Branch" and "Master Branch" are both used in version control systems like Git, but their meanings and implications have evolved over time. 👩‍💻📝

1. **Master Branch**: Historically, the "master" branch was the default and primary branch in many version control systems, including Git. It contained the latest stable version of the code. However, the term "master" has been criticized for its potential racial and discriminatory connotations. As a result, many open-source projects and organizations have moved away from using "master" and adopted more neutral terminology.
    

**Main Branch**: In response to concerns about the term "master," many projects and companies have shifted to using "main" as the default branch name instead. The "main" branch serves the same purpose as the old "master" branch, containing the latest stable version of the codebase

## 3\. Can you explain the difference between Git and GitHub?

**Git** 🐙: Git is a distributed version control system that helps developers track changes in their source code over time. It allows multiple people to collaborate on a project by managing different versions of files and enabling seamless merging of changes. Think of Git as the underlying technology that handles version control, branching, and merging.

**GitHub** 🐱: GitHub, on the other hand, is a web-based platform built around Git. It provides a user-friendly interface for hosting and managing Git repositories. GitHub adds collaboration features like issue tracking, pull requests, code reviews, and project management tools. It's like a social network for developers and a hub for open-source projects.

In simple terms:

* **Git** is the engine that powers version control and code management.
    
* **GitHub** is a platform that uses Git to provide a user-friendly environment for hosting, sharing, and collaborating on code.
    
    ## 4\. How do you create a new repository on GitHub?
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691700315602/8e0fc0f2-613e-490d-a3aa-95a3e424c150.png align="center")

Creating a new repository on GitHub is a straightforward process. Here's a step-by-step guide:

1. **Login or Sign Up**: If you don't have a GitHub account, sign up for one. If you're already logged in, proceed to the next step.
    
2. **Navigate to Your Profile**: After logging in, click on your profile picture in the top right corner of the GitHub homepage. This will open a dropdown menu.
    
3. **Select "Your repositories"**: From the dropdown menu, click on "Your repositories." This will take you to a page that lists your existing repositories.
    
4. **Click "New"**: On the right-hand side of the "Your repositories" page, you'll find a green button labeled "New." Click on it.
    
5. **Fill in Repository Details**:
    
    * **Repository Name**: Choose a name for your repository. This should be a unique and meaningful name that describes your project.
        
    * **Description**: Optionally, add a short description to explain what your repository is about.
        
    * **Visibility**: Choose whether your repository will be public (visible to everyone) or private (visible only to you and collaborators).
        
    * **Initialize with a README**: You can choose to create a new repository with an initial README file. This is often a good idea to provide an overview of your project.
        
    * **Add .gitignore**: You can select a template to automatically ignore certain files (like build artifacts) from being tracked by Git.
        
    * **Add a license**: You can choose a license for your repository to specify how others can use your code.
        
    * **Click "Create Repository"**: Once you've filled in the details, click the green "Create Repository" button at the bottom of the page.
        

## 5\. What is difference between local & remote repository? How to connect local to remote?

A **local repository** and a **remote repository** are two essential components of version control systems like Git. They serve different purposes in managing your codebase and collaborating with others.

**Local Repository**:

* A local repository is the copy of your project's code and version history that resides on your computer's hard drive.
    
* It allows you to work on your code, create branches, make commits, and experiment with changes without affecting the main codebase.
    
* It provides a private workspace for development before sharing changes with others.
    

**Remote Repository**:

* A remote repository is a copy of your project's code that is hosted on a remote server, often on platforms like GitHub, GitLab, or Bitbucket.
    
* It serves as a centralized location for collaboration among team members. Multiple developers can work on the same project and contribute their changes.
    
* It enables you to share your code, collaborate, review changes, and manage the project's overall version history.  
    

## Tasks:

### Task 1: Set your user name and email address, which will be associated with your commits.

```bash
git config --global user.name "Rahil" #for name
git config --global email "skrahil965@gmail.com" #for email
```

### task-2:

### Create a repository named "Devops" on GitHub

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691700995039/9ab53083-04d1-497f-ad16-b99322610c4c.png align="center")

### Connect your local repository to the repository on GitHub.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691701082899/c6601bfd-210e-4560-a090-77aaf651e369.png align="center")

### Create a new file in Devops/Git/Day-02.txt & add some content to it

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691701164085/660698a2-fe2c-4dff-b5ec-de8706fae464.png align="center")

### Push your local commits to the repository on GitHub

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691701211823/76036a17-ee14-4183-9e57-b1c9a1174e71.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1691701233102/fa2d6bc7-e38a-4062-9e2d-a139a67c60fc.png align="center")

> ### **HAPPY LEARNING**
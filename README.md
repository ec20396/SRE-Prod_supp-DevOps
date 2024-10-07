# SRE-Prod_supp-DevOps
## Table of Contents

- [Introduction](#introduction)
- [Course Overview](#course-overview)
- [Activities](#activities)
  - [Set up a Personal GitHub Repository](#activity-set-up-a-personal-github-repository)
  - [Create a GitHub Personal Access Token](#activity-create-a-github-personal-access-token)
  - [AWS EC2 Setup](#activity-aws-ec2-setup)
  - [Linux Exercises: Basic Commands](#activity-linux-exercises-basic-commands)
  - [Linux Tools & Navigation](#activity-linux-tools--navigation)
  - [File Management & Git](#activity-file-management--git)
  - [Editing Files in Linux](#activity-editing-files-in-linux)
  - [Fix Log Analysis](#activity-fix-log-analysis)
  - [File Systems in Linux](#activity-file-systems-in-linux)
  - [Linux Jobs](#activity-linux-jobs)
  - [Scheduling and Automation](#activity-scheduling-and-automation)
  - [Using Vi](#activity-using-vi)
  - [Linux Networking and Sys Admin](#activity-Linux-Networking-and-Sys-Admin)
  - [Linux Advanded Commands](#activity-Linux-Advanced-Commands)
  - [File Permissions in Linux](#activity-File-Permissions-in-Linux)
  - [Linux Variables](#activity-Linux-Variables)
- [Notes](#notes)
- [Resources](#resources)

## Introduction

This repository documents my journey through the Mthree training program to become a Site Reliability Engineer. It includes various projects and exercises that demonstrate the skills and knowledge I have acquired during the training.

## Course Overview

The training program covers a wide range of topics essential for an SRE, including but not limited to:

1. Basic Concepts and Terminology
2. Git Basics
3. Linux Fundamentals
4. Basic Tools and Navigation
5. Monitoring

## Activities

### Activity: Set up a Personal GitHub Repository

**Description:** 
This activity involves [creating a personal GitHub repository](https://docs.github.com/en/get-started/quickstart/create-a-repo) to store and manage your code and projects. Setting up a GitHub repository is a fundamental step for version control and collaboration in software development. This activity covers the steps to create a repository, initialize it with a README file, and make the first commit.

**Key Features:**
- [Creation of a new GitHub repository](https://docs.github.com/en/get-started/quickstart/create-a-repo).
- Initialization of the repository with a README file.
- Making the first commit to the repository.
- Basic understanding of version control using Git and GitHub.

**Files:** 
- [README.md](README.md) (this file)


### Activity: Create a GitHub Personal Access Token

**Description:**
This activity involves creating a GitHub Personal Access Token (PAT) to securely authenticate and authorize access to your GitHub account when performing operations from the command line or other tools. This is crucial for tasks that require elevated permissions, such as pushing changes to repositories or accessing private repositories. Detailed steps can be found in the [GitHub documentation](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

**Key Features:**
- [Generating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).
- Configuring the token for use in command-line operations.
- Understanding the scope and permissions associated with the token.

**Files:**
- No specific files for this activity.


### Activity: AWS EC2 Setup

**Description:**
This activity involves setting up an AWS EC2 instance, which is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the AWS infrastructure. This includes steps to launch, configure, and connect to an EC2 instance. Detailed instructions can be found in the [AWS EC2 documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html).

**Key Features:**
- [Launching an EC2 instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html).
- Configuring security groups and key pairs.
- Connecting to the instance using SSH.
- Basic management and monitoring of the instance.

**Files:**
- No specific files for this activity.


### Activity: Linux Exercises: Basic Commands

**Description:**
This activity covers fundamental Linux commands essential for navigating and managing a Linux environment. These commands form the basis of everyday operations in Linux, such as file management, system navigation, and basic system information retrieval. Detailed explanations and examples can be found in the [Linux Command Line documentation](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).

Complete the following activities using a Linux interface, using skills covered in Linux Lesson 2:

1. Run a command to find your current location on the server.
2. Change directory from your current location to /var/log.
3. Go back up a directory.
4. Find your current location again.
5. List all the files in the current directory.
6. Now list all the files with the long listing.
7. Now list all the files with the long listing in reverse order, with the newest appearing at the bottom of your screen.
8. Change to root directory.
9. Change back to your home directory.
10. Go up a level in directory structure.
11. Find out more information about the ls command.
12. Go back to /var.
13. Show the contents of this directory with details reverse sorted by size (you may have to use `man` to help).
14. Find out the hardware version you are running.

**Key Features:**
- [Basic navigation commands](https://ubuntu.com/tutorials/command-line-for-beginners#2-navigating-the-command-line) (e.g., `cd`, `ls`).
- File manipulation commands (e.g., `cp`, `mv`, `rm`).
- Viewing file contents (e.g., `cat`, `less`, `head`, `tail`).
- Basic system information commands (e.g., `uname`, `top`, `df`).

**Files:**
- [Activity - Linux Exercises - Basic Commands](Activities/Activity%20-%20Linux%20Exercises%20-%20Basic%20Commands.docx)


### Activity: Linux Tools & Navigation

**Description:**
This activity involves practising basic navigation commands in a Linux system. It includes tasks such as checking the current version of Linux, navigating through the file system, and using commands to list files and view command history. Detailed explanations and examples can be found in the [Linux Tools documentation](https://linux.die.net/man/).

Complete the following activities using a Linux interface:

1. Check the current version of Linux:
    ```bash
    uname -a
    ```
2. Check your current location in the file structure:
    ```bash
    pwd
    ```
3. Move up one folder:
    ```bash
    cd ..
    ```
4. Check your location again:
    ```bash
    pwd
    ```
5. List all the files with details. Try both of these commands to see how they are different:
    ```bash
    ls -l
    ls -ltr
    ```
6. Change the directory to the root folder:
    ```bash
    cd /
    ```
7. Check your location again:
    ```bash
    pwd
    ```
8. List all files in the current directory, sorted with the most recently-changed file at the bottom of the screen:
    ```bash
    ls -ltr
    ```
9. Change back to your home directory:
    ```bash
    cd ~
    ```
10. List all files, including the hidden files:
    ```bash
    ls -ltra
    ```
11. Run the history command:
    ```bash
    history
    ```

**Key Features:**
- Practising basic Linux navigation commands.
- Understanding how to list and manage files.
- Using commands to view system information and command history.

**Files:**
- [Activity - Linux Tools & Navigation](Activities/Activity%20-%20Linux%20Tools%20&%20Navigation.md)

### Activity: File Management & Git

**Description:**
This activity focuses on managing files and directories in a Linux environment along with basic Git operations. It includes tasks such as creating, moving, and deleting files and directories, as well as initializing a Git repository, committing changes, and pushing to a remote repository. Detailed explanations and examples can be found in the [Linux File Management documentation](https://www.guru99.com/linux-file-directory-management.html) and [Git documentation](https://git-scm.com/doc).

#### Part A: Managing Files and Folders

1. Create a folder in your home directory using your name as the name of the folder:
    ```bash
    mkdir <yourname>
    ```

2. Move into the folder:
    ```bash
    cd <yourname>
    ```

3. Create an empty file:
    ```bash
    touch test.txt
    ```

4. Create a new folder in this folder called `myfolder`:
    ```bash
    mkdir myfolder
    ```

5. Move the empty file you created into `myfolder`:
    ```bash
    mv test.txt myfolder
    ```

6. Create a backup of the file:
    ```bash
    cp myfolder/test.txt myfolder/test.bkp
    ```

7. Remove the backup file:
    ```bash
    rm myfolder/test.bkp
    ```

8. Go back to your home directory:
    ```bash
    cd ~
    ```

#### Part B: Working with Git

1. Clone the repository:
    ```bash
    git clone https://github.com/TheSoftware-Guild/pss-orderbook-deploy.git
    ```

2. Go to the newly created `pss-orderbook-deploy` directory:
    ```bash
    cd pss-orderbook-deploy
    ```

3. Navigate to the folder `src/linux_activities/Activity2`:
    ```bash
    cd src/linux_activities/Activity2
    ```

#### Searching Files

1. Display the contents of the file `stock_investments.txt`:
    ```bash
    cat stock_investments.txt
    ```

2. Display the first five lines of the file:
    ```bash
    head -5 stock_investments.txt
    ```

3. Display the five last lines of the file:
    ```bash
    tail -5 stock_investments.txt
    ```

4. Display how many times the word GOOG is used:
    ```bash
    grep GOOG stock_investments.txt | wc -l
    ```

5. Display how many lines contain the word T:
    ```bash
    grep -wc T stock_investments.txt
    ```

6. List the files that contain the word SPY in any letter case:
    ```bash
    grep -i SPY *
    ```

7. List the files that do not contain the word SPY:
    ```bash
    grep -L SPY *
    ```

8. Find all files containing the word “data” in their name:
    ```bash
    find . -type f -name "*data*"
    ```

9. Find folders named error:
    ```bash
    find . -type d -name error
    ```

10. Change permissions on all files that contain the word "data" so that the files are read-only for group and other:
    ```bash
    sudo find . -type f -name "*data*" -exec chmod 744 {} \;
    ```

11. Locate and remove write permission for all users on the file named `WFC/data.txt`:
    ```bash
    chmod a-w WFC/data.txt
    ```

**Key Features:**
- Creating, moving, and deleting files and directories using `touch`, `mv`, and `rm`.
- Initializing a Git repository with `git init`.
- Adding files to the staging area with `git add`.
- Committing changes with `git commit`.
- Pushing changes to a remote repository with `git push`.

**Files:**
- [Activity - File Management & Git](Activities/Activity%20-%20File%20Management%20&%20Git.md)


### Activity: Editing Files in Linux

**Description:**
In this activity, you will practise using `vi` to edit files in the PSS Orderbook GitHub repository, which you should have already cloned into your Linux instance. This activity includes tasks such as identifying incorrect prices, adding new data, and using `vi` commands to search and replace text.

**Key Features:**
- Identifying and correcting incorrect prices in a CSV file.
- Adding new data to an existing CSV file.
- Using `vi` shortcuts to search and replace text.
- Practising `vi` navigation and editing commands.

**Files:**
- [Activity - Editing Files in Linux](Activities/Activity%20-%20Editing%20Files%20in%20Linux.md)

### Activity: Fix Log Analysis

**Description:**
This activity involves analysing log files to identify issues, patterns, and potential fixes. It includes tasks such as reading log files, searching for specific keywords, filtering log entries based on time, and extracting relevant information. Detailed explanations and examples can be found in the [Linux Log Management documentation](https://www.guru99.com/log-management.html).

**Key Features:**
- Reading log files using `cat`, `less`, and `tail`.
- Searching for specific keywords using `grep`.
- Filtering log entries based on time using `awk` or `sed`.
- Extracting relevant information and summarising findings.

**Files:**
- [Logs Folder](Activities/Logs/)


### Activity: File Systems in Linux

**Description:**
This activity involves using Linux to examine your system and individual file storage, as well as compress files you create. You will work with file systems, create and manage directories, list and sort files, and compress and decompress files.

**Key Features:**
- Creating and managing directories.
- Listing and sorting files.
- Checking disk usage and free space.
- Creating and extracting tarballs.
- Compressing and decompressing files.

**Files:**
- [Memory Report Folder](Activities/memory_report/)


### Activity: Linux Jobs

**Description:**
In this activity, you will learn how to manage jobs in Linux using commands such as `bg`, `fg`, `jobs`, and `kill`. You will practice running jobs in the foreground and background, switching between them, and terminating jobs. Additionally, you will learn to use the `screen` command to manage multiple terminal sessions.

**Key Features:**
- Running jobs in the foreground and background.
- Viewing and managing background jobs.
- Terminating and bringing jobs back to the foreground.
- Using the `screen` command to manage multiple terminal sessions.

**Files:**
- [Activity - Linux Jobs](Activities/Activity%20-%20Linux%20Jobs.md)

### Activity: Scheduling and Automation

**Description:**
In this activity, you will practice writing some `cron` jobs using the `fixGenerator` script as the command to execute. You will learn how to schedule tasks to run at specific times and intervals using `cron`.

**Key Features:**
- Installing and enabling `cron` on an Amazon Linux2 instance.
- Scheduling tasks to run at various times and frequencies.
- Copying and managing `cron` job configurations.

**Files:**
- [Activity - Scheduling and Automation](Activities/Activity%20-%20Scheduling%20and%20Automation.md)
  
### Activity: Using Vi

**Description:**
This activity involves using `vi` to edit files in the PSS Orderbook GitHub repository, which you should have already cloned into your Linux instance. You will practice editing text files, running word counts, replacing text, and managing lines within files.

**Key Features:**
- Editing files with `vi`.
- Running word counts and replacing text.
- Practicing `vi` navigation and editing commands.

**Files:**
- [Using Vi Folder](Activities/Using%20Vi/)
- [Activity - Using Vi](Activities/Activity%20-%20Using%20Vi.md)

### Activity: Linux Networking and Sys Admin

**Description:**
This activity involves using various Linux commands to perform system administration tasks, including memory management, inode management, and network diagnostics. You will learn to monitor processes, use network diagnostic tools, and manage system resources effectively.

**Key Features:**
- Monitoring memory usage and processes.
- Understanding and managing inodes.
- Using network diagnostic tools like `ping`, `nslookup`, `traceroute`, and `dig`.
- Managing open ports and monitoring network traffic.

**Files:**
- [Activity - Linux Networking and Sys Admin](Activities/Activity%20-%20Linux%20Networking%20and%20Sys%20Admin.md)

### Activity: Linux Advanced Commands

**Description:**
This activity involves using various Linux commands to perform a series of tasks involving file manipulation, text processing, and log management. You will learn to create, modify, and analyze log files using a variety of Linux tools.

**Key Features:**
- Creating and organizing directories.
- Using `sed` for text replacement in files.
- Extracting specific log entries using `grep`.
- Combining log entries into new files.
- Processing log files with `awk` and `sed`.
- Creating comma-separated values (CSV) files.
- Comparing differences between files with `diff`.

**Files:**
- [Activity - Linux Advanced Commands](Activities/Activity%20-%20%20Linux%20Advanced%20Commands.md)

## Activity: File Permissions in Linux

**Description:**

This activity guides you through the process of managing file permissions in a Linux environment. You will learn how to create and manage user accounts, assign permissions to files and directories, and understand the significance of different permission settings. The activity involves practical exercises such as creating a new user, modifying group memberships, and using commands to control access to files and directories.

**Key Features:**
- **User Management:** Create and configure a new user account.
- **Password Management:** Set and expire passwords for the new user.
- **Sudoers Configuration:** Add the new user to the sudoers file to grant administrative privileges.
- **Directory and File Management:** Create directories and files, change ownership, and modify permissions.
- **Group Management:** Create and manage user groups, and assign group ownership to directories.
- **Permission Settings:** Use `chmod` to change file and directory permissions, allowing different levels of access.
- **Script Execution:** Create and manage executable scripts with controlled permissions.

**Files:**
- [Activity - File Permissions in Linux](Activities/Activity%20-%20File%20Permissions%20in%20Linux.md)

## Activity: Linux Variables

**Description:**

This activity focuses on understanding and managing environment variables in a Linux environment. You will learn how to create, modify, and delete environment variables, understand the significance of different variable types, and explore the impact of these variables on the system and user sessions. This activity includes practical exercises such as creating environment variables, modifying shell profiles, and managing variables within scripts.

**Key Features:**
- **Environment Variable Management:** Learn how to create, export, and modify environment variables.
- **Profile Configuration:** Modify the `~/.bash_profile` or `~/.bashrc` files to set persistent environment variables.
- **Script Execution:** Create and manage scripts that utilize environment variables.
- **PATH Management:** Understand and modify the `PATH` variable to include custom directories.
- **Variable Scope:** Explore the differences between local and exported variables, and how they affect subprocesses.
- **Aliases and Functions:** Create and manage shell aliases and functions using environment variables.
- **Session Management:** Understand how environment variables persist across different sessions and how to manage them.

**Files:**
- [Activity - Linux Variables](Activities/Activity%20-%20Linux%20Variables.md)


## Notes

Personal notes and summaries of important concepts covered during the training.

**Files:**

## Resources

A list of additional resources that were helpful throughout the training program.


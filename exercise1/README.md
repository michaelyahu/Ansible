**Exercise 1: File Management Automation with Ansible**
-

**Description**
-
    In this exercise, I implemented file management automation using Ansible,
    a popular configuration management tool,
    on a Hyper-V environment with virtual machines running CentOS.
    The entire process was executed via SSH connections through Visual Studio (VS) between the machines.
    The goal was to transfer files from one server to another,
    ensure that the files were successfully transferred,
    and perform checks on the settings, permissions, and ownership of the files.

**Content**


    - Transferring files from one server to another.
    - Configuring permissions for the transferred files.
    - Checking the existence of the files to confirm successful transfer.

**Playbook content**

    - Ensure test directory exists.
    - Copy file with owner and permissions.
    - Check that if details.txt exists.
    - Rename details.txt to info.txt.
    - Check permissions and ownership of the info.txt file.
    - Get user information.
    - Get group information.
    - Debug for the steps & Debug file ownership and permissions.

**Troubleshoot**

    During the project, I encountered several issues that I had to resolve to make the automation work.

    Security - I had to create a security certificate for the Controller server and implement it on the Target1 server 
    to perform the operation without the need for authentication.

    Permissions - I dealt with permission issues when transferring files, for example, 
    when the user did not have sufficient permissions to copy files to a specific directory.

    DEBUG - During the work, I was unsure where the process was halting, so I had to add DEBUG statements
    for each action to understand where each action was stopping and, if it did stop, what was preventing it from continuing.

**Snapshots of Automation: Key Steps in the Project**
-

![Hyper-V](https://github.com/michaelyahu/Ansible/blob/main/exercise1/env-vm.png?raw=true)

![result](https://raw.githubusercontent.com/michaelyahu/Ansible/729a1686d7a3c625993f1b70be3392d3e3c909bc/exercise1/Screenshot%202024-10-16%20130341.png)


    

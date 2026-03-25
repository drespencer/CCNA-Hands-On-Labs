Modifying File and Directory Ownership

Purpose

This lab focused on practicing how to change file and directory ownership in Linux. The scenario involved organizing a colleague’s files into a centralized directory and assigning the correct ownership so the user could manage their own workspace. The goal was to reinforce how ownership affects access, why administrative privileges are sometimes required, and how to apply chown correctly in a real system‑administration workflow.

Topology Overview

All tasks were completed in a Linux terminal on the Client1 virtual machine. The work centered around the /home directory structure, where I created a new directory path and adjusted ownership to match the intended user.

Key Configurations

I created a new directory at /home/work_files/pat using elevated privileges since my account did not have permission to write directly under /home. After verifying that the directory was created with root as the default owner, I reassigned ownership to the user pat using the chown command. This ensured that Pat could manage the directory and its contents without requiring administrative intervention.

Verification Commands

I used ls -l to confirm directory creation and ownership changes. Viewing the long listing allowed me to verify that root initially owned the directory and that ownership successfully transferred to the pat account after running chown. Re‑running the command after each step helped validate that the changes applied correctly.

Troubleshooting Notes

A key reminder from this lab is that directories created with sudo default to root ownership, which can block the intended user from accessing or modifying their workspace. Verifying ownership immediately after creation prevents access issues later. Using chown with the full directory path ensures the correct target is modified, and rechecking with ls -l confirms the change before moving on.

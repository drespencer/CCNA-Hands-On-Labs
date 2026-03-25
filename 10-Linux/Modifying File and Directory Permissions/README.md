Modifying File and Directory Permissions

Purpose
This lab focused on strengthening my understanding of Linux file and directory permissions. I walked through how ownership, groups, and permission bits control access, and practiced modifying those permissions using both symbolic and numeric modes. The goal was to build confidence in managing access control in a multi‑user environment and reinforce core system‑administration fundamentals.

Topology Overview
This lab was completed in a Linux command‑line environment. All tasks were performed directly in the terminal, working with files and directories to observe how permission changes affect access and behavior.

Key Configurations
I reviewed and modified permissions using the standard Linux permission model, focusing on three access categories: owner, group, and others. I worked with read, write, and execute permissions and applied changes using chmod in both symbolic and numeric formats. I also changed file and group ownership using chown and explored how directory permissions differ from file permissions, especially regarding traversal and content modification.

Verification Commands
I used ls -l to verify permission changes and confirm ownership. I tested access behavior after modifying permissions to ensure the results matched expectations. This included checking whether files could be read, written, or executed, and whether directories could be entered or modified based on the assigned permissions.

Troubleshooting Notes
A key takeaway was recognizing how missing execute permissions on directories can block access even when read permissions are present. I also reinforced the importance of verifying ownership before adjusting permissions, since incorrect ownership can cause unexpected access issues. When permission‑denied errors occurred, reviewing the permission string and confirming the user’s relationship to the file (owner, group member, or other) helped quickly identify the root cause.

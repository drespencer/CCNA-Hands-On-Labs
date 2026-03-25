Setting User Access to Files

Purpose

This lab focused on managing user access to files in a Linux environment. I practiced assigning and adjusting permissions so that specific users could read, write, or execute files as needed. The goal was to reinforce how Linux enforces access control and how to apply permission changes safely in a real system‑administration workflow.

Topology Overview

All tasks were completed in a Linux terminal on the Client1 virtual machine. The work centered around a set of files that required different access levels for different users. I used standard Linux permission tools to configure and verify the correct access for each user.

Key Configurations

I reviewed existing permissions using ls -l to understand the current access model. From there, I applied changes using chmod in both symbolic and numeric modes to grant or restrict read, write, and execute permissions. I also worked with chown and chgrp when ownership or group membership needed to be updated to support the required access.

Verification Commands

I used ls -l after each change to confirm that permissions were applied correctly. I also tested access by switching users or attempting actions that should be allowed or denied based on the updated permissions. This helped validate that the permission model matched the intended access requirements.

Troubleshooting Notes

A key reminder from this lab is that permissions alone don’t guarantee access-ownership and group membership also matter. When a user couldn’t access a file even after permissions were updated, checking the file’s owner and group helped identify the issue. Another important point was ensuring execute permissions were set when users needed to run scripts or enter directories.

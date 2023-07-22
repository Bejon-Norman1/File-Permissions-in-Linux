# File Permissions in Linux

## Project Description

The research team at my organization needed to update the file permissions for certain files and directories within the projects directory. The permissions did not currently reflect the level of authorization that should be given, and ensuring appropriate permissions was crucial for system security. To accomplish this task, I performed the following key responsibilities:

## Responsibilities

### 1. Check File and Directory Details

I utilized Linux commands to determine the current permissions set for a specific directory in the file system. By employing the `ls` command with the `-la` option, I obtained a detailed listing of the file contents, including hidden files. This information helped in assessing the current permissions and identifying the areas that required modification.

### 2. Describe the Permissions String

The 10-character string representing permissions can be deconstructed to understand the authorized access and specific permissions for users. This knowledge enabled me to interpret the permissions effectively, distinguishing between directories and regular files and identifying read, write, and execute permissions for users, groups, and others.

### 3. Change File Permissions

Based on the organization's requirements, I modified file permissions to ensure compliance. By using the `chmod` command, I removed or added specific permissions for users, groups, and others as necessary. This process aligned file access with the organization's security policies.

### 4. Change File Permissions on Hidden Files

For hidden files, such as those starting with a period (.), I made adjustments to meet the organization's access preferences. By utilizing the `chmod` command, I altered permissions to restrict write access for certain users while preserving read access for others.

### 5. Change Directory Permissions

In accordance with the organization's directives, I adjusted directory permissions to provide exclusive access to specific users. By employing the `chmod` command, I removed execute permissions for unauthorized users while preserving them for designated users.

## Summary

By effectively checking, interpreting, and modifying file and directory permissions, I successfully matched the required level of authorization as per the organization's preferences for the projects directory. Utilizing Linux commands and the `chmod` function, I ensured a secure and compliant file system environment.

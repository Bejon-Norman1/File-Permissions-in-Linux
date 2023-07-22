# File Permissions in Linux

## Project Description

The research team at my organization required updates to file permissions for specific files and directories within the projects directory. The existing permissions did not align with the desired level of authorization, and ensuring appropriate permissions was crucial for system security. To accomplish this task, I performed the following key responsibilities:

## Responsibilities

### 1. Check File and Directory Details

![Screenshot 2023-07-21 200736](https://github.com/Bejon-Norman1/File-Permissions-in-Linux/assets/19808403/d1169f71-b239-4771-9e29-98ac7f59be2c)


I utilized Linux commands to determine the current permissions set for a specific directory in the file system. By employing the `ls` command with the `-la` option, I obtained a detailed listing of the file contents, including hidden files. This information helped in assessing the current permissions and identifying the areas that required modification.

### 2. Describe the Permissions String

The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:

- 1st character: This character is either a `d` or hyphen (`-`) and indicates the file type. If it’s a `d`, it’s a directory. If it’s a hyphen (`-`), it’s a regular file.

- 2nd-4th characters: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the user. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted to the user.

- 5th-7th characters: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the group. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted for the group.

- 8th-10th characters: These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for others. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (`-`) instead, that indicates that this permission is not granted for others.

For example, the file permissions for `project_t.txt` are `-rw-rw-r--`. Since the first character is a hyphen (`-`), this indicates that `project_t.txt` is a file, not a directory. The second, fifth, and eighth characters are all `r`, which indicates that the user, group, and others all have read permissions. The third and sixth characters are `w`, which indicates that only the user and group have write permissions. No one has execute permissions for `project_t.txt`.

### 3. Change File Permissions

Based on the organization's requirements, I modified file permissions to ensure compliance. By using the `chmod` command, I removed or added specific permissions for users, groups, and others as necessary. This process aligned file access with the organization's security policies.

### 4. Change File Permissions on Hidden Files

For hidden files, such as those starting with a period (.), I made adjustments to meet the organization's access preferences. By utilizing the `chmod` command, I altered permissions to restrict write access for certain users while preserving read access for others.

### 5. Change Directory Permissions

In accordance with the organization's directives, I adjusted directory permissions to provide exclusive access to specific users. By employing the `chmod` command, I removed execute permissions for unauthorized users while preserving them for designated users.

## Summary

By effectively checking, interpreting, and modifying file and directory permissions, I successfully matched the required level of authorization as per the organization's preferences for the projects directory. Utilizing Linux commands and the `chmod` function, I ensured a secure and compliant file system environment.

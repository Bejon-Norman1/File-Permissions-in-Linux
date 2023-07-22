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

The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined  `project_t.txt` must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:

![Screenshot 2023-07-21 202040](https://github.com/Bejon-Norman1/File-Permissions-in-Linux/assets/19808403/c8ba9c41-2e72-48ee-934e-3cbfee95b7f9)

The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The `chmod` command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the `project_k.txt file`. After this, I used `ls` `-la` to review the updates I made.

### 4. Change File Permissions on Hidden Files

The research team at my organization recently archived `project_x.txt`. They do not want anyone to have write access to this project, but the user and group should have read access.

The following code demonstrates how I used Linux commands to change the permissions:

![Screenshot 2023-07-22 003043](https://github.com/Bejon-Norman1/File-Permissions-in-Linux/assets/19808403/313d5d98-584a-4fad-bfe1-3c586c1d5e9f)


The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I know `.project_x.txt` is a hidden file because it starts with a period `(.)`. In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with `u-w`. Then, I removed write permissions from the group with `g-w`, and added read permissions to the group with `g+r`.

### 5. Change Directory Permissions

My organization only wants the `researcher2` user to have access to the drafts directory and its contents. This means that no one other than `researcher2` should have execute permissions.

The following code demonstrates how I used Linux commands to change the permissions:

![Screenshot 2023-07-22 003736](https://github.com/Bejon-Norman1/File-Permissions-in-Linux/assets/19808403/40212266-6505-408c-a418-18ac430aff3b)

The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I previously determined that the group had execute permissions, so I used the `chmod` command to remove them. The `researcher2` user already had execute permissions, so they did not need to be added.

## Summary

To align with my organization's desired level of authorization, I made several adjustments to the permissions of files and directories within the projects directory. Here's a summary of the steps I followed:

1. Checked Current Permissions: I began by using the `ls -la` command to inspect the existing permissions for the directory. This allowed me to understand the initial setup and informed my subsequent decisions.

2. Modifying Permissions: Based on the information gathered in step 1, I used the `chmod` command multiple times to modify the permissions of specific files and directories as per the organization's requirements.

By following this process, I successfully achieved the desired level of security and access control for the files and directories in the projects directory.


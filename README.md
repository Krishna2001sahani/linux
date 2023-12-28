internsctl is a custom Linux command created to perform various operations on your server. This command provides functionalities related to CPU information, memory information, user management, and file information.

Manual Page
To view the full documentation, execute:

bash
man internsctl
Help
To see usage guidelines and examples, use the following command:
internsctl --help
Version
To check the version of the command, use:
internsctl --version
Section A
1. CPU Information
internsctl cpu getinfo
Expected Output:
Similar to the output from the lscpu command.

2. Memory Information
internsctl memory getinfo
Expected Output:
Similar to the output from the free command.

Section B
Part 1 | Level Easy
Create a New User
internsctl user create <username>
Note:
This command creates a user who can log in to the Linux system and access their home directory.

List Regular Users
internsctl user list
List Users with Sudo Permissions
internsctl user list --sudo-only
Part 2 | Level Intermediate
Get File Information
internsctl file getinfo <file-name>
Expected Output:

makefile

File: <file-name>
Access: <permissions>
Size(B): <file-size>
Owner: <file-owner>
Modify: <last-modified-time>
Part 3 | Advanced Level
Get Specific Information About a File

internsctl file getinfo [options] <file-name>
Options:

--size, -s: Print file size
--permissions, -p: Print file permissions
--owner, -o: Print file owner
--last-modified, -m: Print last modified time
Expected Output with Options:

To obtain the size of the specified file:

internsctl file getinfo --size <file-name>
Output:
<file-size>

To obtain the permissions of the specified file:

internsctl file getinfo --permissions <file-name>
Output: <file-permissions>

To obtain the owner of the specified file:

internsctl file getinfo --owner <file-name>
Output: <file-owner>

To obtain the last modified time of the specified file:

internsctl file getinfo --last-modified <file-name>
Output: <last-modified-time>

Contributing
Feel free to contribute to this project by submitting issues or pull requests.

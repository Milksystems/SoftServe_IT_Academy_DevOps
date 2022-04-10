Task2

1) Analyze the structure of the /etc/passwd and /etc/group file, what fields are present in it, what users exist on the system? Specify several pseudo-users, how to define them?

![image](https://user-images.githubusercontent.com/97533533/162631683-8c9f969f-c14d-4076-86a6-f465a9880d2c.png)

![image](https://user-images.githubusercontent.com/97533533/162631715-78c7bbfb-0f5a-4892-b598-4dfcae50d2c7.png)

Pseudo user (UID 1-499)

Pseudo users are related to system and program services Any Linux system has these pseudo users by default Mail news games, Apache FTP, MySQL and sshd are related to the process of Linux system Pseudo users usually do not need or cannot log in to the system There can be no host directory

2) What are the uid ranges? What is UID? How to define it?

UID stands for user identifier. A UID is a number assigned to each Linux user. It is the user’s representation in the Linux kernel. The UID is used for identifying the user within the system and for determining which system resources the user can access.

Superuser (root uid = 0)

General user (UID 500-60000)

Pseudo user (UID 1-499)

The id command in Linux will display the UID, GID and groups your current user belongs to

![image](https://user-images.githubusercontent.com/97533533/162631793-9ab68667-b170-4370-8cb2-63436ff49063.png)

3) What is GID? How to define it?

Group ID (GID)

In addition to the user ID, the account has a group ID associated with it. User groups are used to organize access of several users to some resources. A group, like a user, has a name and an identification number - GID (Group ID).

![image](https://user-images.githubusercontent.com/97533533/162631883-b318e9b7-9e6f-4c05-98c3-0ac2ce5e8ae6.png)

4) How to determine belonging of user to the specific group?

![image](https://user-images.githubusercontent.com/97533533/162631917-787bf0a2-c6b5-4d31-9844-178618e521c2.png)

5) What are the commands for adding a user to the system? What are the basic parameters required to create a user?

new user:

/sudo useradd test

create him a password:

/sudo passwd test

create home directory:

/sudo useradd -m test

creating a user with specific home directory:

/sudo useradd -m -d /path_name test

creating a user with specific User ID:

/sudo useradd -u 1500 test

creating a user with an expiry date:

/sudo useradd -e 2022-05-04 test

creating a user and assign multiple groups:

/sudo useradd -g users -G wheel,developers test

6) How do I change the name (account name) of an existing user?

sudo usermod -l test1 test

7) What is skell_dir? What is its structure?

Directory /etc/skel/ (skel is derived from the “skeleton”) is used to initiate home directory when a user is first created. A sample layout of “skeleton” user files is as shown below:

![image](https://user-images.githubusercontent.com/97533533/162632526-f7a9248b-878d-4265-99e7-9adbaf4b79f5.png)

8) How to remove a user from the system (including his mailbox)?

sudo userdel -r test

9) What commands and keys should be used to lock and unlock a user account?

First way using passwd

to lock:
   
/sudo passwd -l test
   
to unlock:
   
/sudo passwd -u test

Second way using usermod
   
to lock:
   
/sudo usermod -L test
   
to unlock: 
   
/sudo usermod -U test

10) How to remove a user's password and provide him with a password-free login for subsequent password change?

test ALL=(ALL) NOPASSWD:ALL

11) Display the extended format of information about the directory, tell about the information columns displayed on the terminal.

![image](https://user-images.githubusercontent.com/97533533/162632886-34a9d95f-c96c-4a68-95ea-46290fc7009e.png)

Displays permissions, links, owner, group, size, time, name.

12) What access rights exist and for whom (i. e., describe the main roles)? Briefly describe the acronym for access rights.

![image](https://user-images.githubusercontent.com/97533533/162632959-0acb485f-3411-4b10-9279-3d9169813c1c.png)

13) What is the sequence of defining the relationship between the file and the user?

By default, the owner of a file is the user who created it and the group assigned to a file is the primary group of the user.

14) What commands are used to change the owner of a file (directory), as well as the mode of access to the file? Give examples, demonstrate on the terminal.

sudo chown root hard_link_labwork2

15) What is an example of octal representation of access rights? Describe the umask command.

When a file is created, the permission flags are set according to the file mode creation mask, which can be set using the umask command. The file mode creation mask (sometimes referred to as "the umask") is a three-digit octal value whose nine bits correspond to fields 2-10 of the permission flags.

16) Give definitions of sticky bits and mechanism of identifier substitution. Give an example of files and directories with these attributes.

The sticky bit was initially introduced to ‘stick’ an executable program’s text segment in the swap space even after the program has completed execution, to speed up the subsequent runs of the same program. However, these days the sticky bit means something entirely different.

When a directory has the sticky bit set, its files can be deleted or renamed only by the file owner, directory owner and the root user.

17) What file attributes should be present in the command script?

![image](https://user-images.githubusercontent.com/97533533/162633256-2f76c65e-699f-416a-ae16-3e056aa5ce07.png)

The files and directories can have following attributes:

![image](https://user-images.githubusercontent.com/97533533/162633264-e63e48bc-fd73-4b4f-96ec-4c6f4672481e.png)
















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
   
   sudo passwd -l test
   
   to unlock:
   
   sudo passwd -u test

Second way using usermod
   
   to lock:
   
   sudo usermod -L test
   
   to unlock: 
   
   sudo usermod -U test






























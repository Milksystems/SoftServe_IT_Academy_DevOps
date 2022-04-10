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


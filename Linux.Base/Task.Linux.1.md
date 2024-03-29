Task1.Part1

1) Log in to the system as root.

![image](https://user-images.githubusercontent.com/97533533/161798159-fccb85cc-4095-4fa3-9eb3-0e3c34038cdb.png)

2) Use the passwd command to change the password. Examine the basic
parameters of the command. What system file does it change *?

![image](https://user-images.githubusercontent.com/97533533/161799882-67ba8ad7-3d1d-405f-b6c7-bc6db69748e7.png)

3) Determine the users registered in the system, as well as what commands they execute. What additional information can be gleaned from the command execution?

![image](https://user-images.githubusercontent.com/97533533/162586423-dcecdb6f-da50-4466-8351-f5c595fb468b.png)

Also we can use next commands for describe users in system - "w", "who" and "whoami".

![image](https://user-images.githubusercontent.com/97533533/162586471-a43739cb-79a7-4a40-8e27-26d7f08cc262.png)

4) Change personal information about yourself.

![image](https://user-images.githubusercontent.com/97533533/162586556-a165c558-fb14-4e14-b3ba-87559bd05ae3.png)

5) Become familiar with the Linux help system and the man and info commands. Get help on the previously discussed commands, define and describe any two keys for these commands. Give examples.

![image](https://user-images.githubusercontent.com/97533533/162586637-d0df86ef-ab84-4289-9480-f1b820ec06ed.png)

![image](https://user-images.githubusercontent.com/97533533/162586751-411e59cc-5f1b-48a1-b1dc-57c5488106b2.png)

6) Explore the more and less commands using the help system. View the contents of files .bash* using commands.

![image](https://user-images.githubusercontent.com/97533533/162586844-26490651-624b-40de-94b9-34cb54a51f03.png)

7) Describe in plans that you are working on laboratory work 1. Tip: You should read the documentation for the finger command.

![image](https://user-images.githubusercontent.com/97533533/162586900-757a7a37-9649-4e5b-8325-09e53859b9d0.png)

8) List the contents of the home directory using the ls command, define its files and directories. Hint: Use the help system to familiarize yourself with the ls
command.

![image](https://user-images.githubusercontent.com/97533533/162587106-372feb3b-d910-4670-8699-1f28d160f8a6.png)

This command help me list all files in my home directory. Key -a - helpful for show all files and directories, key -I - shows all as one list with columns, key -h - allows to see information on a human-readable format, key --group-directories-first - allows to sort listing and seeing group of directories before files.

Task1.Part2

1) Examine the tree command. Master the technique of applying a template, for example, display all files that contain a character c, or files that contain a
specific sequence of characters. List subdirectories of the root directory up to and including the second nesting level.

![image](https://user-images.githubusercontent.com/97533533/162587206-8f1b7316-e45f-432d-82c4-bf28b633ceac.png)

2) What command can be used to determine the type of file (for example, text or binary)? Give an example.

![image](https://user-images.githubusercontent.com/97533533/162587266-32646c44-1a27-4eaf-bd62-73a23c6c333a.png)

3) Master the skills of navigating the file system using relative and absolute paths. How can you go back to your home directory from anywhere in the filesystem?

![image](https://user-images.githubusercontent.com/97533533/162587355-3fca808f-ce59-4d95-a9f1-ba41e31e4a5d.png)

4) Become familiar with the various options for the ls command. Give examples of listing directories using different keys. Explain the information displayed on
the terminal using the -l and -a switches.

I amswered this question in point 8 of part 1 of this Task.

5) Perform the following sequence of operations:
- create a subdirectory in the home directory;
- in this subdirectory create a file containing information about directories
located in the root directory (using I/O redirection operations);
- view the created file;
- copy the created file to your home directory using relative and absolute
addressing.
- delete the previously created subdirectory with the file requesting removal;
- delete the file copied to the home directory.

![image](https://user-images.githubusercontent.com/97533533/162627441-acadb152-9b90-4b07-a949-ead20ffe6115.png)

![image](https://user-images.githubusercontent.com/97533533/162627643-36ada535-a20a-44c5-b643-75db2a3f397c.png)

![image](https://user-images.githubusercontent.com/97533533/162627858-9f3a089a-bbbf-4d5e-b6b3-80ce9cb3e754.png)

6) Perform the following sequence of operations:
- create a subdirectory test in the home directory;
- copy the .bash_history file to this directory while changing its name to labwork2;
- create a hard and soft link to the labwork2 file in the test subdirectory;
- how to define soft and hard link, what do these concepts;
- change the data by opening a symbolic link. What changes will happen and why?
- rename the hard link file to hard_lnk_labwork2;
- rename the soft link file to symb_lnk_labwork2 file;
- then delete the labwork2. What changes have occurred and why?

![image](https://user-images.githubusercontent.com/97533533/162628179-55ae0ffd-9847-48d6-82be-063cd17daa59.png)

![image](https://user-images.githubusercontent.com/97533533/162628220-ef540a35-1c5a-4236-9947-b80b1e2fe07d.png)

![image](https://user-images.githubusercontent.com/97533533/162628232-01f2eb61-fd43-45f2-b96b-4ffb0fa26817.png)

![image](https://user-images.githubusercontent.com/97533533/162628292-027d0fbe-4e05-4110-a9f3-1fc12f576b0a.png)

![image](https://user-images.githubusercontent.com/97533533/162628327-fd2a7b56-11b8-4309-ad7c-dee91f438270.png)

![image](https://user-images.githubusercontent.com/97533533/162628399-f5347ebc-09da-4e73-93ec-974efe0e303c.png)

![image](https://user-images.githubusercontent.com/97533533/162628857-a221e1ff-978d-4108-8ac3-b8271fc9f719.png)

![image](https://user-images.githubusercontent.com/97533533/162628873-8483a271-d187-4b8a-9159-46a53570d877.png)

These are the commands I used:

![image](https://user-images.githubusercontent.com/97533533/162629224-92772019-a7bb-45b4-a50f-d103c77f468e.png)

Hardlink - it's a link, what specify path not to the file, but to the recording itself on a filesystem, hardlinks works only in one partition and don't be used in a network path or from another drive, hardlinks works only with files and not work with folders. Symbolic link or Symlink - it's like a windows shortcat file (.Ink), she only specify path to file, but she works with network paths, different partitions and folders. How described in our example - when file was changed, text in hard and soft links equal text in originsl file, but when we delete original file - hardlink is working (because he know where file in harddrive) and symlink is not works, because she losses the file, what specified in she's path.

7) Using the locate utility, find all files that contain the squid and traceroute sequence.

![image](https://user-images.githubusercontent.com/97533533/162629344-e35a671d-fc6d-432b-9cf4-01f15471f6cf.png)

8) Determine which partitions are mounted in the system, as well as the types of these partitions.

![image](https://user-images.githubusercontent.com/97533533/162629389-e045d810-8451-458a-85e1-fdc4a87a8b63.png)

9) Count the number of lines containing a given sequence of characters in a given file.

![image](https://user-images.githubusercontent.com/97533533/162629498-32b6486f-03b7-498e-a865-cc0ef35c6fd6.png)

10) Using the find command, find all files in the /etc directory containing the host character sequence.

![image](https://user-images.githubusercontent.com/97533533/162629652-2790a89c-f522-4599-babb-cdd4601f233c.png)

![image](https://user-images.githubusercontent.com/97533533/162629700-2cc2f868-9b4d-4cf3-b623-4e258a5f4bb5.png)

11) List all objects in /etc that contain the ss character sequence. How can I duplicate a similar command using a bunch of grep?

![image](https://user-images.githubusercontent.com/97533533/162629823-9d54e86e-b63a-4371-a4ce-43d614df6e66.png)

12) Organize a screen-by-screen print of the contents of the /etc directory. Hint: You must use stream redirection operations.

![image](https://user-images.githubusercontent.com/97533533/162630024-7cdd4868-ceca-4c6f-8479-c06379cf06df.png)

13) What are the types of devices and how to determine the type of device? Give examples.

![image](https://user-images.githubusercontent.com/97533533/162630362-73b88e38-43a7-4fd0-9ab5-a505f3cd960d.png)

14) How to determine the type of file in the system, what types of files are there?

Linux contains 7 types of files: Regular - denoted by symbol "-" Directory - denoted by symbol "d" Link File - denoted by symbol "I" Character DEvice File - denoted by symbol "c" Local Socket File - denoted by symbol "s" Named Pipe File - denoted by symbol "p" Block Device File - denoted by symbol "b".

15) List the first 5 directory files that were recently accessed in the /etc directory.

![image](https://user-images.githubusercontent.com/97533533/162631488-2526a9f8-8a26-4785-9144-635713cf46fe.png)

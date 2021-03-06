1) Analyze the structure of the /etc/passwd and /etc/group file, what fields are
   present in it, what users exist on the system? Specify several pseudo-users, how
   to define them?
2) What are the uid ranges? What is UID? How to define it?

   - A UID (user identifier) is a number assigned by Linux to each user on the system. 
     This number is used to identify the user to the system and to determine which system resources the user can access.

   - UID 0 (zero) is reserved for the root.
   - UIDs 1–99 are reserved for other predefined accounts.
   - UID 100–999 are reserved by system for administrative and system accounts.
   - UID 1000+ are used for user accounts.
   
   - GIDs are stored in the /etc/passwd file

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-3.gif)

3) What is GID? How to define it?

   - Groups in Linux are defined by GIDs (group IDs).

   - GID 0 (zero) is reserved for the root group.
   - GID 1–999 are reserved for the system and application use.
   - GID 1000+ allocated for the user’s group.

   - GIDs are stored in the /etc/groups file

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-2.gif)

4) How to determine belonging of user to the specific group?
   
   - `groups username`
   - `id username`

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-4.gif) 

5) What are the commands for adding a user to the system? What are the basic
   parameters required to create a user?

   - `useradd -m username`
   - `passws -e username`
   - `adduser username`

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-5.gif)

6) How do I change the name (account name) of an existing user?

   - `sudo usermod -l newUsername oldUsername`

   - `sudo usermod -d /home/newHomeDir -m newUsername`

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-6.gif)

7) What is skell_dir? What is its structure?

   - skel is derived from the skeleton because it contains basic structure of home directory
   - The /etc/skel directory contains files and directories that are automatically copied over to a new user’s when
      it is created from useradd command.
   - This will ensure that all the users gets same intial settings and environment.

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-7.gif)

8) How to remove a user from the system (including his mailbox)?

  - `sudo userdel -r username`

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-8.gif)

9) What commands and keys should be used to lock and unlock a user account?
   - `passwd -l username`
   - `passwd -u username`
   - or
   - `usermod -L username`
   - `usermod -U username`

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-9.gif)

10) How to remove a user's password and provide him with a password-free
    login for subsequent password change?

   - sudo passwd -e osboxes

![image](https://github.com/pronetware-it/DevOps_for_Unix/blob/main/linux-base/Task-2/2-10.gif)

11) Display the extended format of information about the directory, tell about
    the information columns displayed on the terminal.
12) What access rights exist and for whom (i. e., describe the main roles)?
    Briefly describe the acronym for access rights.
13) What is the sequence of defining the relationship between the file and the
    user?
14) What commands are used to change the owner of a file (directory), as well
    as the mode of access to the file? Give examples, demonstrate on the terminal.
15) What is an example of octal representation of access rights? Describe the
    umask command.
16) Give definitions of sticky bits and mechanism of identifier substitution. Give
    an example of files and directories with these attributes.
17) What file attributes should be present in the command script?

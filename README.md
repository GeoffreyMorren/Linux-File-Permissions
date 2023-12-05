<h1 align="center">
  File permissions in Linux
</h1>

<p align="center">
  <strong>Project description</strong>
</p>

<p align="center">
  The goal of this project is to get familiar and gain experience using Linux commands to manage file permissions.
</p>

<h2 align="center">
  Check file and directory details
</h2>

<p align="center"><img src="https://github.com/GeoffreyMorren/Linux-File-Permissions/assets/152500568/0f4cbc7b-2e84-4fca-8766-f76a5fd4e716" /></p>

<p align="center">
  <strong>Describe the permissions string</strong>
</p>

<p align="center">
  The .project_x.txt example in the image above is a hidden file (shown by the . in front of the name). This file has the following permissions assigned:<br>
  User (researcher2): read, write<br>
  Group (research_team): write<br>
  Other: none
</p>

<p align="center">
  The drafts directory has the following permissions assigned:<br>
  User: read, write, executable<br>
  Group: executable<br>
  Other: none
</p>

<h2 align="center">
  Change file permissions
</h2>

<p align="center">
  The organization does not allow others to have write access to any files.
</p>

<p align="center"><img src="https://github.com/GeoffreyMorren/Linux-File-Permissions/assets/152500568/0944b3d3-90fc-4cd4-9987-e44446cbd489" /></p>

<p align="center">
  <strong>Change file permissions on a hidden file</strong>
</p>

<p align="center">
  The research team has archived .project_x.txt, which is why it’s a hidden file. This file should not have write permissions for anyone, but the user and group should be able to read the file.
</p>

<p align="center"><img src="https://github.com/GeoffreyMorren/Linux-File-Permissions/assets/152500568/d23b194c-f115-4a58-a5d4-89c021c40c7f" /></p>

<p align="center">
  <strong>Change directory permissions</strong>
</p>

<p align="center">
  The files and directories in the projects directory belong to the researcher2 user. Only researcher2 should be allowed to access the drafts directory and its contents.
</p>

<p align="center"><img src="https://github.com/GeoffreyMorren/Linux-File-Permissions/assets/152500568/643af28d-36a2-4494-ae03-e963686b48e3" /></p>

<h2 align="center">
  Summary
</h2>

<p align="center">
  I used the pwd command to see in which directory I was correctly working. As I needed to make changes to the projects directory, I used the cd command to move to the right directory. Since the goal was to change the permissions in the projects directory, I used the ls -la command to get a list of the current assigned permissions for the project directory, including the hidden files. With the chmod command, I changed the permissions as requested. The 10 character strings are built as such that the d stands for a directory and a - stands for a file (a . in front of a file name meaning it is a hidden file). This allowed me to identify and make a graphical representation of how the project directory was built. After the first character, the strings are built of 3 character blocks that represent user, group, and other permissions. The permissions for each either being r (read), w (write) or x (executable). A - would mean no permission.
</p>

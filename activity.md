Git Intro Activity
==================

A. Form teams
-------------

Form a 2-person team. Try to find someone who uses the same platform as you (e.g., Windows, Linux, etc.). If you can't, that's fine. If you are the odd-person-out, join a team of 2.

Assign the following roles to the members of your team. If you are in a
team of 2, assign the recorder and navigator roles to the same person.

Roles:

-   Driver: Creates and maintains a local git repository.

-   Navigator: Reads instructions and records answers.

3rd person role (if you have a 3-person team):

-   Quality Assurance Person: Ensures instructions are being carried out correctly, answers are clear, and looks for ways for the team to work together more effectively.

You will be rotating roles. Your instructor will let you know when to switch roles. Switching roles requires switching computers. So, plan accordingly.


B. Setup
-------------

1. Create and share a shared document (Google Doc, Etherpad, etc.) for your team.
2. Copy and paste this document into your shared document.

C. Download and install Git
---------------------------

Download and install Git for your operating system:

-   <https://git-scm.com/downloads>

Starting a terminal:

-   **Windows**:

    -   git-bash.exe (Linux style commands)

    -   git-cmd.exe (Windows style commands)

-   **Mac OSX:** Finder -&gt; Applications -&gt; Utilities -&gt;
    Terminal.app

-   **Linux:** will vary depending on your window manager

D. Getting help
---------------

Run the following commands.

    git help
    git help -ag
    git help init

1.  What does `git help` do?

    ```


    ```

2.  What does `-ag` cause `git help` to do?

    ```



    ```

E. Identify yourself
--------------------

Run the following commands, replacing BOGUS NAME and BOGUS@EMAIL with
your name and email.

    git config --global user.name 'BOGUS NAME'
    git config --global user.email 'BOGUS@EMAIL'

WARNING: The name and email you give will be listed on each commit you make.
If this repository is ever published, your name and email on every commit
will be too. Also, if you are working on a shared computer, you should
consider changing this configuration before you walk away.


1.  What are these commands doing?

    ```



    ```

2.  What is the purpose of `--global`?

    ```



    ```

F. Create a repository
From the command line, run the following commands.

bash
Copy
Edit
mkdir first_project
cd first_project
1. By default, any file that starts with . is hidden. How do you display a hidden file?
On Mac/Linux, run:

bash
Copy
Edit
ls -a
On Windows (Git Bash), run:

bash
Copy
Edit
ls -la
2. Run this command to show the hidden files in the current directory. Are there any?
Before running git init, there are no hidden Git-related files.

3. Now run the following command.
csharp
Copy
Edit
git init
4. Check for hidden files again. What was created by git init?
A hidden .git directory was created, which contains all Git metadata and version control history.

5. What do you think would happen if you delete .git?
Deleting .git will remove all version history, making the project no longer a Git repository.

6. Using your observations from previous questions, how can you determine if a project is managed using Git?
Run:

bash
Copy
Edit
ls -a
If there is a .git directory, it is a Git repository. Alternatively, running:

lua
Copy
Edit
git status
will confirm if the directory is under version control.

G. Basic commands
Use a plain text editor to create names.txt inside the first_project folder. Put the names of your team in the file. Save and exit.

Run git status before and after each of these commands.

pgsql
Copy
Edit
git add names.txt
git commit -m "Add our names."
git log
1. What kind of information does git status report?
It shows the state of the working directory and staging area, indicating which files are modified, staged, or untracked.

2. What does git add names.txt do?
It stages names.txt for the next commit.

3. What does git commit -m "Add our names." do?
It commits the staged changes with the message "Add our names.", creating a new version in the repository.

Use a plain text editor to create the following files:

birthdays.txt - Put your birthdays in this file.
movies.txt - Put the last movie each of you watched in alphabetical order.
Run git status before and after each of these commands.

pgsql
Copy
Edit
git add .
git commit
git log
4. What does git add . do? What do you think . means?
git add . stages all changes (new, modified, or deleted files) in the current directory. The . refers to the entire directory.

5. What does git commit (without -m) do?
It opens the default text editor for writing a multi-line commit message.

6. If you want to write a more detailed commit message, what command would you use?
Use:

sql
Copy
Edit
git commit
This opens an editor for writing a multi-line commit message.

7. What does git log do?
It displays the commit history, including commit messages, authors, and timestamps.

H. Stage/Cache/Index
Modify names.txt and movies.txt, then create foods.txt.

Run:

csharp
Copy
Edit
git add names.txt
git status
1. Categorize the state of each file:
Staged:

Copy
Edit
names.txt
Unstaged:

Copy
Edit
movies.txt
Untracked:

Copy
Edit
foods.txt
2. If you run git commit, what changes will be committed?
Only staged changes (names.txt) will be committed.

3. What command do you run to stage changes?
csharp
Copy
Edit
git add <filename>
4. What command do you run to unstage changes?
perl
Copy
Edit
git reset <filename>
Run:

css
Copy
Edit
git diff
git diff --cached
5. What does git diff display?
It shows differences between the working directory and the last commit.

6. What does git diff --cached display?
It shows differences between the staging area and the last commit.

I. Undo
Run:

pgsql
Copy
Edit
git reset --soft HEAD^
1. What does git reset --soft HEAD^ do?
It moves the last commit to the staging area but keeps file changes.

Run:

pgsql
Copy
Edit
git reset --hard HEAD^
2. What does git reset --hard HEAD^ do?
It completely removes the last commit and all changes.

3. What is the difference between --hard and --soft?
--soft keeps changes in the staging area, while --hard deletes them.

4. What does HEAD refer to?
It refers to the current commit.

5. What does HEAD^ mean?
It refers to the previous commit.

J. Helpful resources
--------------------

-   <https://git-scm.com/doc>

-   <https://www.atlassian.com/git/tutorials/>

-   <https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf>

K. Copyright and Licensing
--------------------------

Copyright 2016, Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike
4.0 International License. To view a copy of this license, visit
<http://creativecommons.org/licenses/by-sa/4.0/> .

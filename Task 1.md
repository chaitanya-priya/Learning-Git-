# Task 1 

#### Question 1: What is VCS ? Why is it important ?

VCS stands for version control system. It is like a database that stores a snapshot of your complete project at any given point.  When you take a look at an older version of your project, it let's you compare the past and the current one. It shows any differences if they exist between the two of the versions of your project. 

VCS is platform independent. It does not depend on what platform, technology or framework used when the project is done. It saves any version you create, record it and save the changes that one has made and let them compare with the already created version of the project. 

#### Question 2: How to clone a Git repository ? 

  Steps to clone Git repository: 

1.  Once GitHub is open, navigate to the main page which has the repository you want to download. 
2. Under the repository, you will be provided with an option to clone or download. In the Clone with HTTPs section, click an icon next to the link to copy the clone URL for the repository.
3. Open Git Bash.
4. Change the current working directory to the location where you want the cloned directory to be made.
5. Type `git clone', and then paste the URL that was copied in the step before.
6. Press Enter. Your local clone will be created. 

#### Question 3: How to pull or push to remote repository ?

#### Question 4: How to check the status of of repository ? 

The status of a repository can be checked by running the command 'git status'. The command reports back the status of the repository. 

#### Question 5: How to create and switch to a branch ?

1. From your terminal window, list the branches on your repository.

   The output obtained says that there is a single branch, the master and asterisk indicated that the branch is currently active. 

2. Create a new feature branch in the repository

   $ git branch <feature_branch>`

3. Switch to the feature branch to work on it.

   `$ git checkout <feature_branch>`

   You can list the branches again with the `git branch` command.

4. Commit the change to the feature branch:

   `$ git add . $ git commit -m "adding a change from the feature branch"`

5. Switch back to the `master` branch.

   `$ git checkout master`

6. Push the feature branch to Bitbucket:

   `$ git push origin <feature_branch>`

7. View the **Source** page of your repository in Bitbucket. You should see both the `master` and the feature branch. When you select the feature branch, you see the **Source** page from that perspective. Select the feature branch to view its **Recent commits**.

#### Question 6: How to connect to a remote a repository ? 

When you clone a repository from a remote server, Git automatically remembers this connection for you. It saves it as a remote called "origin" by default.
In other cases where you started with a fresh local repository, no remote connections are saved. In that situation, we need to connect our local repository to a new remote before we can try some remote interactions:

```
$ git remote add crash-course-remote 
    https://github.com/gittower/git-crash-course-remote.git
```

#### Question 7: How to merge two branch ? 

`git merge` takes two commit pointers, usually the branch tips, and will find a common base commit between them. Once Git finds a common base commit it will create a new "merge commit" that combines the changes of each queued merge commit sequence.

#### Question 8: How to resolve merge conflicts ? 

Conflicts occur when changes are made to the same line by two different people. Similarly, conflicts could also arise if one person edits a file and another deletes it.

Git provides three ways of resolving conflicts:

- Aborting the merge

  **git merge –abort**

  This command will abort the merge process and get you out of the conflict.

- Resolving conflicts manually

  For resolving conflicts manually, you need to look at the file and remove the unwanted version changes in the file. Also remove >>>>>>Head & ====== from the lines and make sure that the file has proper code syntax. Save and commit the file.When you are between merge states, you do not need to write a commit message. Just type **git commit** and the pop-up window will indicate the conflict in the files. Remove the lines to resolve the conflict.

- Using Tools

  Simply type **git mergetool** and you will see thee list of available tools.

  #### Question 9: How to commit changes ? 

  **The "commit" command is used to save your changes to the local repository.**

  Note that you have to explicitly *tell* Git which changes you want to include in a commit *before* running the "git commit" command. This means that a file won't be *automatically* included in the next commit just because it was changed. Instead, you need to use the "git add" command to mark the desired changes for inclusion.

  #### Question 10: How to stash changes ?

  `git stash`  command is used to stash changes.

  
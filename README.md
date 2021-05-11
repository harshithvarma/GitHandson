# GitHandson


# 1) Diiference between Git and SVN

  GIT: Git is an open-source distributed vice control system developed by Linus Torvalds in 2005. Its emphasis on speed and data integrity in which there is no centralized     connectivity is needed. It is powerful and cheap branching with easy merge in which each developer has his repository and have a local copy in which they can change history. It  supports non-linear development branches and applications with a large number of codes files.
    
  SVN: Apache Subversion is an open-source software version and revision control system under the Apache license. It managed files and folders that are present in the  repository. It can operate across the network, which allows it and used by people on different computer .we can say that a repository is like an ordinary file server which allows it to be used by people on a different computer.
    
# 2) Git commands and their usages

  git config - This command sets the author name and email address respectively to be used with your commits.
  git init - This command is used to start a new repository.
  git clone - This command is used to obtain a repository from an existing URL.
  git add - This command adds a file to the staging area.
  git commit - This command records or snapshots the file permanently in the version history.
  git diff - This command shows the file differences which are not yet staged.
  git reset - This command unstages the file, but it preserves the file contents.
  git status - This command lists all the files that have to be committed.
  git merge - This command merges the specified branch’s history into the current branch.
  git remote - This command is used to connect your local repository to the remote server.
  git push - This command sends the committed changes of master branch to your remote repository.
  git pull - This command fetches and merges changes on the remote server to your working directory.
  git stash - This command temporarily stores all the modified tracked files.
  
 # 3) Git Config
 The most basic use case for git config is to invoke it with a configuration name, which will display the set value at that name. Configuration names are dot delimited strings composed of a 'section' and a 'key' based on their hierarchy. For example: user.email
 The git config command can accept arguments to specify which configuration level to operate on. The following configuration levels are available:

--local
By default, git config will write to a local level if no configuration option is passed. Local level configuration is applied to the context repository git config gets invoked in. Local configuration values are stored in a file that can be found in the repo's .git directory: .git/config
 

 --global
Global level configuration is user-specific, meaning it is applied to an operating system user. Global configuration values are stored in a file that is located in a user's home directory. ~ /.gitconfig on unix systems and C:\Users\\.gitconfig on windows
 

 --system
System-level configuration is applied across an entire machine. This covers all users on an operating system and all repos. The system level configuration file lives in a gitconfig file off the system root path. $(prefix)/etc/gitconfig on unix systems. On windows this file can be found at C:\Documents and Settings\All Users\Application Data\Git\config on Windows XP, and in C:\ProgramData\Git\config on Windows Vista and newer.

Thus the order of priority for configuration levels is: local, global, system. This means when looking for a configuration value, Git will start at the local level and bubble up to the system level.

# 4)Explain the different points when a merge can enter a conflicted stage. What is the difference between fork, branch, and clone

Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict. Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.
   # Git fails to start the merge
   A merge will fail to start when Git sees there are changes in either the working directory or staging area of the current project. Git fails to start the merge because these pending changes could be written over by the commits that are being merged in. When this happens, it is not because of conflicts with other developer's, but conflicts with pending local changes. The local state will need to be stabilized using git stash, git checkout, git commit or git reset
   
   # Git fails during the merge
   A failure DURING a merge indicates a conflict between the current local branch and the branch being merged. This indicates a conflict with another developers code. Git will do its best to merge the files but will leave things for you to resolve manually in the conflicted files.
   
   Forking is done on the GitHub Account while Cloning is done using Git. When you fork a repository, you create a copy of the original repository (upstream repository) but the repository remains on your GitHub account. Whereas, when you clone a repository, the repository is copied on to your local machine with the help of Git.
   Forking is a concept while cloning is a process. Forking is just containing a separate copy of the repository and there is no command involved. Cloning is done through the command ‘git clone‘ and it is a process of receiving all the code files to the local machine.
   A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

The git branch command lets you create, list, rename, and delete branches. It doesn’t let you switch between branches or put a forked history back together again. For this reason, git branch is tightly integrated with the git checkout and git merge commands.

# 5) What is the difference between rebasing and merge in Git?
 If you would prefer a clean, linear history free of unnecessary merge commits, you should reach for git rebase instead of git merge when integrating changes from another branch.

On the other hand, if you want to preserve the complete history of your project and avoid the risk of re-writing public commits, you can stick with git merge. Either option is perfectly valid, but at least now you have the option of leveraging the benefits of git rebase.
   
   
  
   


 




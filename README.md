# Git Notes

> git pull

> git fetch

> git merge

> git commit --amend -m "message"
- Once we have done a commit and forget or want to add more changes on existing but want to commit in same that time --amend is used.

> git rm -f [filename]
- It removes the file from local repository

> git stash
- The git stash command in Git is used to save changes that have not been committed yet but are not ready to be committed or to switch to a different branch. 
- Stashing allows you to save your changes temporarily and revert your working directory to a clean state. 
- Later, you can reapply the stashed changes.

- git stash save "Your stash message" : To stash your local changes
- git stash list : You can see a list of your stashes
- git stash apply : To reapply the most recent stash
- git stash apply stash@{1} : If you have multiple stashes, you can specify a stash by index
- git stash pop : If you want to apply and remove the most recent stash in one step
- git stash drop stash@{1} : To remove a specific stash without applying its changes
- git stash branch <new-branch-name> : If you stashed changes on one branch and want to apply them to a different branch

> git rev-list
- lists commit objects in reverse chronological order. It provides a way to view commits in various ways, and it can be used for filtering and formatting commit information.
- git rev-list main
- git rev-list --count main
- git rev-list --max-count=1 main

> git clean
- The git clean command is used to remove untracked files and directories from the working directory
- git clean -nfd : show romoving status of file and folder
- git clean -f : remove files from working directory 
- git clean -fd : remove directories with files from working directory

> git config --global alias.<alias-name> '<git-command>'
- They allow you to create shorter or more convenient names for commonly used Git commands or command sequences. 
- git config --global alias.ck checkout  
	git ck dev

> help.autocorrect (git config --global help.autocorrect <time-in-tenths-of-seconds>)
-  allows you to enable automatic correction of typos in Git commands. This can be useful in situations where you mistype a Git command, and Git can automatically correct it to the closest valid command if the typo is close enough.
- Replace <time-in-tenths-of-seconds> with the time (in tenths of seconds) Git should wait before autocorrecting.
- git config --global help.autocorrect 10 : wait for 10s
- git config --global help.autocorrect 0 : Setting the wait time to 0 effectively disables autocorrection

> git cherry-pick <commit-hash>
- It allows you to select specific commits from one branch and apply them to another branch
- git cherry-pick 81fd6ac

> git reset
- The git reset command in Git is used to reset the current branch to a specific state. 
- git reset --soft HEAD^ (<commit-hash>) : reset to staging to commit
- git reset --mixed HEAD^ (<commit-hash>) : reset to working directory to commit
- git reset --hard HEAD^ (<commit-hash>) : remove commit from local repository

> git reflog <branch-name>
- The git reflog command in Git is a powerful tool that helps you review the history of branch references, including the movements of branch pointers and commit references.
- The term "reflog" is short for "reference log."
- git reflog --relative-date main
- git reflog show main

> git blame <file-path>
- used to display information about who last modified each line of a file and when the modification was made.
- It helps you track the authorship and changes to each line in a file over time.


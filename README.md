### GIT BASIC COMMANDS

•	git status (Status of the files in the working directory)

•	git add . 
  git add <filename> (Move unstaged files to staging area)
 
•	git commit -m “….” (Move staging area files to commit objects folder)
•	git config <commands> (Configuration of git)

•	git log (Log of the working directory)
  git log --merge ( Logging the conflict merge operation to understand which commits have conflict in the branches )

•	git checkout <commit ID> ( Changes current wd to the related commit) <br>
  git checkout <branchName> ( Changes current wd to the related branch) <br>
  git checkout -b <branchName> ( Creates a new branch and changes current wd to the new branch ) <br>
  git checkout . ( Undo Unstaged changes) <br>
  git checkout <fileName> ( Undo Unstaged changes of a specific file) <br>

•	git branch (List all branches)<br>
  git branch <branchName> (Creates new branch)<br>
  git branch -d <branchName> (Deletes branch)<br>
  git branch -D <branchName> (Force delete branch)<br>

•	git merge <branchName> (Merges the branch with the current branch that we are in)
  git merge --squash <branchName> ( Combines all commits to one commit in the target branch and stages it to source branch )
  git merge --no-ff <branchName> ( Recursive merge: If any commit has been made after creating the merged target branch we use recursive merge ) 
  git merge --abort (Aborts the merge operation; useful in merge conflict situations )

•	git cherry-pick <commit ID> ( adding the change in the commit to the target branch)

•	git reset <fileName> (Bring back the latest status before changes)
  git reset --soft HEAD~<go back step count> (HEAD commits goes back by the count)
  git reset  HEAD~<go back step count> (HEAD commits and latest stage adds goes back by the count but stays in wd)
  git reset --hard  HEAD~<go back step count> (HEAD commits and latest stage adds goes back by the count and changes are deleted in wd)
  git reset --hard <hashed ID from reflog> ( Reseting the project to the hashed ID status )

### GIT ADDITIONAL COMMANDS
•	git switch <branchName> ( Changes current wd to the related branch )
  git switch -c <branchName> > ( Creates a new branch and changes current wd to the new branch )
 
•	git ls-files (List of staging area files)
•	git rm <fileName> ( Deletes the file from staging area)

•	git restore . ( Undo Unstaged changes)
  git restore <fileName> ( Undo Unstaged changes of a specific file)
  git restore --staged <fileName> ( Undo staged changes of a specific file)


•	git clean -dn (Lists all untracked files to be removed)
  git clean -df (Deletes all untracked files)
  git restore --staged <fileName> ( Undo Unstaged changes of a specific file)

•	git diff (Tells the differences of the merge conflicts )
 
 
![image](https://user-images.githubusercontent.com/50409645/172053705-1b9efc32-021a-45ad-a675-5a3edb2b2ab0.png)

## GIT DEEPER COMMANDS

•	git stash ( Reserving the changes into RAM without staging or committing for after commit )
  git stash push -m “….” ( Stashing the changes with a message )
  git stash apply ( Gets the latest stashed changes to the wd in order to stage and commit – STACK / LIFO)
  git stash apply <index> (Gets the specific index from stash list )
  git stash pop <index> ( Gets the specific index from stash list and removes it from stash list )
  git stash list ( Gets the list of stashed changes )
  git stash drop <index> ( Removes the index from stash list )
  git stash clear ( Empties git stash list )

•	git reflog ( List of all actions of git )

•	git tag <tagName> <commit ID> ( Adding tag fort he specific commit )
  git tag ( Shows tag list)
  git tag -d <tagName> ( Deletes the tag with the specified name )
  git tag -a <tagName> -m “….” ( Adds a tag with annotation)
 
•	git Show <tagName> ( Shows the details of the commit with specified tag name )

![image](https://user-images.githubusercontent.com/50409645/172053832-02772cbb-f541-4d8d-acce-2495ace4395c.png)


> :warning: **When you are running the git commands on terminal please omit single quotes;<br/>
> Ex: git add test.txt

### GIT BASIC COMMANDS
<pre>
git status ( Status of the files in the working directory(wd) )

git add . 
git add 'filename' ( Move unstaged files to staging area )
 
git commit -m “….” ( Move staging area files to commit objects folder )

git config 'commands' ( Configuration of git )

git log (Log of the working directory )
git log --merge ( Logging the conflict merge operation to understand which commits have conflict in the branches )

git checkout 'commit ID' ( Changes current wd to the related commit )
git checkout 'branchName' ( Changes current wd to the related branch )
git checkout -b 'branchName' ( Creates a new branch and changes current wd to the new branch )
git checkout . ( Undo Unstaged changes )
git checkout 'fileName' ( Undo Unstaged changes of a specific file )

git branch (List all branches)
git branch -a ( Lists all branches all local tracking, remote tracking and local )
git branch -r ( Lists all remote tracking branches )
git branch 'branchName' (Creates new branch)
git branch -d 'branchName' ( Deletes branch )
git branch -D 'branchName' ( Force delete branch )
git branch --track 'branchName' 'remoteBranchName' ( Creates a local tracking branch for a remote branch )
git branch -vv ( Detailed list of local branches )
git branch --delete --remotes 'alias'/'branchName' ( Deletes remote tracking branch )

git merge 'branchName' (Merges the branch with the current branch that we are in )
git merge --squash 'branchName' ( Combines all commits to one commit in the target branch and stages it to source<br/> branch )
git merge --no-ff 'branchName' ( Recursive merge: If any commit has been made after creating the merged target branch<br/> we use recursive merge ) 
git merge --abort (Aborts the merge operation; useful in merge conflict situations )

git cherry-pick 'commit ID' ( adding the change in the commit to the target branch )

git reset 'fileName' (Bring back the latest status before changes )
git reset --soft HEAD~'go back step count' (HEAD commits goes back by the count )
git reset  HEAD~'go back step count' (HEAD commits and latest stage adds goes back by the count but stays in wd )
git reset --hard  HEAD~'go back step count' ( HEAD commits and latest stage adds goes back by the count and changes<br/> are deleted in wd )
git reset --hard 'hashed ID from reflog' ( Reseting the project to the hashed ID status )
</pre>
### GIT ADDITIONAL COMMANDS
<pre>
git switch 'branchName' ( Changes current wd to the related branch )
git switch -c 'branchName' ( Creates a new branch and changes current wd to the new branch )
 
git ls-files (List of staging area files)
git ls-remote ( List of all remote branches including the branches that are not existed in local )

git rm 'fileName' ( Deletes the file from staging area )

git restore . ( Undo Unstaged changes )
git restore 'fileName' ( Undo Unstaged changes of a specific file )
git restore --staged 'fileName' ( Undo staged changes of a specific file )

git clean -dn ( Lists all untracked files to be removed )
git clean -df ( Deletes all untracked files )

git diff ( Tells the differences of the merge conflicts )
</pre>

### GIT DEEPER COMMANDS
<pre>
git stash ( Reserving the changes into RAM without staging or committing for after commit )
git stash push -m “….” ( Stashing the changes with a message )
git stash apply ( Gets the latest stashed changes to the wd in order to stage and commit – STACK / LIFO )
git stash apply 'index' (Gets the specific index from stash list )
git stash pop 'index' ( Gets the specific index from stash list and removes it from stash list )
git stash list ( Gets the list of stashed changes )
git stash drop 'index' ( Removes the index from stash list )
git stash clear ( Empties git stash list )

git reflog ( List of all actions has been made in the git repository )

git tag 'tagName' 'commit ID' ( Adding tag fort he specific commit )
git tag ( Shows tag list)
git tag -d 'tagName' ( Deletes the tag with the specified name )
git tag -a 'tagName' -m “….” ( Adds a tag with annotation)
 
git show 'tagName' ( Shows the details of the commit with specified tag name )
 </pre>
### GITHUB COMMANDS
<pre>
git remote add 'alias' 'url' ( Connects remote repository; git to Github by an url; “origin” is default alias of the<br/> repository in Github )
git remote ( Lists all remote aliases )
git remote Show 'alias' ( Show detailed configuration of the remote alias )

git push 'alias' 'branch' ( Pushes the code to the remote repository branch through alias and creates a new remote<br/> branch if it does not exist )
git push -u 'alias' 'branch' ( Pushes the code to the remote repository branch through alias, creates both a track<br/> and a new remote branch if it does not exist )
git push 'alias'  --delete 'branchName' ( Deletes remote branch and remote tracking branch if it exists )
git push --force 'alias' 'branchName' ( Pushes the code by force, it does not care if the pushed code is behind<br/> remote code )

git pull 'alias' 'branch' ( Pulls the code to local by merging the changes )

git fetch 'alias' ( Pulls the code to local without merging the changes)

git clone 'repo URL' ( Downloads all default branch files of repository into local directory )
git clone 'branchName' 'repo URL' ( Downloads all specific branch files of repository into local directory )
</pre>


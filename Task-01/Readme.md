To start with,   
git clone https://gitexercises.fracz.com/git/exercises.git  
cd exercises  
git config user.name "Amala B"  
git config user.email "amalababurajan13@gmail.com"  
./configure.sh  
git start  
# generally used:
**git status:**  
**git log**:  
**git branch**
# master  
**COMMANDS USED**  
**git verify**: used to check progress  
# commit-one-file
**COMMANDS USED**  
**git add A.txt**: to add A.txt only  
**git commit -m "Commit only one"**:  
commit the change made, and -m is used to add a commit message in the same line.  
# commit-one-file-staged
**COMMANDS USED:**  
**git reset A.txt**:  
file is unstaged but changes are not lost.  
**git commit -m "Commit only B"** :  
commit the change made  
# ignore-them
**nano gitignore**:  
.gitignore file specifies the untracked files.
Create a file in editable form  
Add content as *.extension(the extensions that is to be excluded  
To ignore whole directory use directory_name/.  
**.gitignore contains:**  
*.o  
*.exe  
*.jar  
libraries/  
**git add .gitignore**;  
to add file to the staging area  
**git commit -m "Ignore files"**:  
to commit changes  
# chase branch
**git reset --hard escaped:**  
reset moves the branch pointer.  
--hard deletes uncommited changes.  
# merge-conflict
**git merge another-peice-of-work:**  
to combine all the commits from current branch to specified one.  
Then, a conflicts arises (in equation.txt)  
**nano equation.txt:**  
open editor, resolve conflict  
**git commit -m "Solved":**  
to copmmit changes.  
# save-your-work
**git stash:**  
to save task without commiting.  
**nano bug.txt:**  
open editor and fix a bug  
**git add bug.txt:**  
add bug.txt to the staging area.  
**git commit -m "bug fixed":**  
to commit changes  
**git stash pop:**  
restores previous changes before bugfix.  
**nano bug.txt:**
open editor, and add Finally, work finished!.  
**git add bug.txt:**  
to add file to the staging area.  
**git commit -m "finished":**  
to commit changes.  
# change-branch-history
First check, current branch is change-branch-history.  
**git rebase hot-bugfix:**  
rebase is used todo commit of change-branch-history only after the commits from hot bug-fix.  
# remove-ignored
**git rm ignored.txt:**  
remove file from repository and working area, then **commit**.  
# case-sensitive-filename
**git mv File.txt file.txt:**  
to move file from File.text to file.txt (Here used to rename the file), then **commit**.  
# fix-typo
**git commit --amend:**  
to change the last commit.  
# forge-date
**git commit --amend --no-edit --date="1987-08-03":**  
--no-edit is used when we dont want to edit.  
# fix old-typo
**git rebase -i HEAD~2:**  
to edit last two commits, in editor it will be something starting with a pick, change pick to edit for the one we want to edit.  
**nano file.txt:**  
to correct the typo in file.txt, then **add**.
**git commit --amend:**  
to edit the message.  
**git rebase --continue:**  
move on to next commit in sequence.  







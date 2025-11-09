# GIT EXERCISES
These exercises deepened my knowledge about git and introduced me to new commands.  
# To start:   
git clone https://gitexercises.fracz.com/git/exercises.git  
cd exercises  
git config user.name "..."  
git config user.email "..."  
./configure.sh  
git start  
# Frequently used:
**git status:**  
to see the current state of working directory.  
**git log**:  
to see the commit history.  
**git branch**  
shows the list of branches in repository.  
# Exercise:01   master  
**COMMANDS USED**  
**git verify**: used to check progress  
# Exercise-02   commit-one-file
**COMMANDS USED**  
**git add A.txt**: to add A.txt only  
**git commit -m "Commit only one"**:  
commit the change made, and -m is used to add a commit message in the same line.  
# Exercise-03   commit-one-file-staged
**COMMANDS USED:**  
**git reset A.txt**:  
file is unstaged but changes are not lost.  
**git commit -m "Commit only B"** :  
commit the change made  
# Exercise-04   ignore-them
**COMMANDS USED**  
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
# Exercise-05   chase branch
**COMMANDS USED**  
**git reset --hard escaped:**  
reset moves the branch pointer.  
--hard deletes uncommited changes.  
# Exercise-06   merge-conflict
**COMMANDS USED**  
**git merge another-peice-of-work:**  
to combine all the commits from current branch to specified one.  
Then, a conflicts arises (in equation.txt)  
**nano equation.txt:**  
open editor, resolve conflict  
**git commit -m "Solved":**  
to copmmit changes.  
# Exercise-07   save-your-work
**COMMANDS USED**  
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
# Exercise-08   change-branch-history
**COMMANDS USED**  
First check, current branch is change-branch-history.  
**git rebase hot-bugfix:**  
rebase is used todo commit of change-branch-history only after the commits from hot bug-fix.  
# Exercise-09   remove-ignored
**COMMANDS USED**  
**git rm ignored.txt:**  
remove file from repository and working area, then **commit**.  
# Exercise-10   case-sensitive-filename
**COMMANDS USED**  
**git mv File.txt file.txt:**  
to move file from File.text to file.txt (Here used to rename the file), then **commit**.  
# Exercise-11   fix-typo
**COMMANDS USED**  
**git commit --amend:**  
to change the last commit.  
# Exercise-12   forge-date
**COMMANDS USED**  
**git commit --amend --no-edit --date="1987-08-03":**  
--no-edit is used when we dont want to edit.  
# Exercise-13   fix old-typo
**COMMANDS USED**  
**git rebase -i HEAD~2:**  
to edit last two commits, in editor it will be something starting with a pick, change pick to edit for the one we want to edit.  
**nano file.txt:**  
to correct the typo in file.txt, then **add**.
**git commit --amend:**  
to edit the message.  
**git rebase --continue:**  
move on to next commit in sequence.  
# Exercise-14   commit-lost
**COMMANDS USED**  
**git reflog:**  
helps to see and recover past work.  
Here we can see the reflog reference(here HEAD@{1}).  
**git reset --hard HEAD@{1}**  
we can see HEAD@{n} from reflog.  
# Exercise-15   split-commit
**COMMANDS USED**  
**git reset HEAD~1:**  
to only remove the commit, but the changes on the work remains same.  
then, add **add first.txt** and **commit**.  
then, add **add second.txt** and **commit**.  
# Exercise-16   too-many-commits
**COMMANDS USED**  
**git rebase -i HEAD~2:**  
unstage only the specific one.  
edit will open, and change second commit from pick to squash.  
# Exercise-17   executable
**COMMANDS USED**  
**chmod +x script.sh:**  
+x to make the file executable.  
Then, **add** and **commit**.  
# Exercise-18   pick-your-features
**COMMANDS USED**  
**git add -p file.txt:**  
to stage parts of changes.
Remove the lines which has no task1 in it.  
Then **commit** and **add work.txt and file.txt.  
# Exercise-19   pick-your-features
**COMMANDS USED**  
**git cherry-pick feature-a**  
**git cherry-pick feature-b**  
**git cherry-pick feature-c**  
to move the current branch forward.  
then, a conflict occurs in program.txt, resolve conflict.  
then, **add** program.txt  
**git cherry-pick --continue:**  
to continue the cherry-pick.  
# Exercise-20   rebase-complex
**COMMANDS USED**  
**git rebase issue-555 --onto your-master:**  
git takes commits in  issue-555 branch on top of your-master branch.  
# Exercise-21   invalid-order
**COMMANDS USED**  
**git rebase -i HEAD~2:**  
to move the second commit up.  
then, an editor appears , swap the order between commits.  
# Exercise-22   find-swearwords
**COMMANDS USED**  
**git log -Sshit:**  
-S is for search for changes that add or remove a string.  
**git rebase -i xxxxxxx^:**  
Open words.txt and list.txt then **add** and **committ**   
**git rebase --continue:**   
move forward after edit.  
# Exercise-23   find-bug
**COMMANDS USED**  
**git bisect:**  
find commit that introduced a bug.  
**git bisect bad HEAD:**  
current commit contains bug.  
**git bisect good 1.0:**  
bug is not there.  
**git bisect run sh -c "openssl enc -base64 -A -d < home-screen-text.txt | grep -v jackass":**  
git bisect run will automatically test each commit by the command we give.  
openssl enc -base64 -A -d < home-screen-text.txt , turns encoded file into readable format.  
grep -v jackass , grep is to search the word, -v means to look for lines without the word.  






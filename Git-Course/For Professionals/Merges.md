# Conflicts in Git

Conflicts occur when changes from different branches cannot be automatically merged by Git.

Identifying Conflicts
When you try to merge branches and Git encounters conflicts, it will pause and inform you which files have conflicts.

Attempt to merge branches

`git checkout main`

`git merge feature-branch`

Git will indicate conflicts in specific files

## Resolving Conflicts

Open the conflicted files and look for markers (<<<<<<<, =======, >>>>>>>) indicating conflicting changes.

Edit the files to manually resolve the conflicts.
plaintext
Copy code
Current changes
Remove conflict markers and keep the desired code.
Marking Conflicts as Resolved
After resolving conflicts, you need to mark the files as resolved and commit the changes.

Add resolved files to the staging area

`git add resolved-file.cpp`

Commit the merge

`git commit -m "Resolve merge conflict between main and feature-branch"`

## Common Commands for Conflict Resolution

Abort the merge if you want to cancel it

`git merge --abort`

Continue the merge after resolving conflicts

`git merge --continue`

Rebase conflicts can be resolved similarly

`git rebase feature-branch`

### Resolve conflicts

#### Continue the rebase

`git rebase --continue`

## Tips for Avoiding Conflicts

Communicate with your team to avoid simultaneous changes in the same files.

Pull changes frequently from the main branch to keep your branch up-to-date.

Make small, frequent commits to reduce the risk of conflicts.
These steps and tips help manage and resolve conflicts efficiently in Git.

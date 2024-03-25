### Git Init (Initialize Git):
  - To start version controlling a project with Git, you need to initialize a Git repository in the project directory.
  - This is done using the `git init` command, which creates a hidden `.git` directory in the project folder.
  - Once initialized, Git begins tracking changes made to files in that directory, enabling version control functionality.

### Git Add:
  - `git add` is a command used to stage changes for the next commit in Git.
  - It adds modified, deleted, or new files to the staging area, preparing them to be included in the next commit.
  - Files can be added individually (`git add filename`) or in bulk (`git add .` to add all changes).

  ### Amend Commits:
  - Git allows you to amend commits, which means making changes to the last commit.
  - This can be useful for correcting mistakes in the commit message or adding more changes to the previous commit.
  - The `git commit --amend` command is used for amending commits, allowing you to edit the commit message and add more changes.

  ### Git Push:
  - `git push` is a command used to push your local commits to a remote repository.
  - It updates the remote repository with changes made locally, making them accessible to others.
  - Syntax: `git push <remote> <branch>`, where `<remote>` is the name of the remote repository and `<branch>` is the branch to push.

### Git Pull:
  - `git pull` is a command used to fetch and merge changes from a remote repository to your local repository.
  - It updates your local repository with changes made remotely, ensuring your local copy is up-to-date.
  - Syntax: `git pull <remote> <branch>`, where `<remote>` is the name of the remote repository and `<branch>` is the branch to pull from.

  ### Git Rebase:
  - `git rebase` is the command used to perform a rebase in Git.
  - It offers flexibility in modifying commit history, such as rearranging or cleaning up commits before integrating them into a branch.

  ### Git Pod:
  - GitPod is an online integrated development environment (IDE) that is fully powered by Git.
  - It allows developers to create, review, and manage Git repositories entirely within a web browser.
  - GitPod provides a convenient way to work with Git repositories without the need for local development environments.

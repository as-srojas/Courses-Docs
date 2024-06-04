### How Git Works:
  - Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
  - It tracks changes in files, allowing multiple people to collaborate on projects without overwriting each other's work.
  - Git works by creating a repository (repo) where it stores all the changes made to files over time, enabling users to revert back to previous versions if needed.

### Installing Git:
  - Git can be installed on various operating systems including Windows, macOS, and Linux.
  - Installation methods vary depending on the operating system, but generally involve downloading the Git installer and following installation prompts.

### Verify Installation:
  - After installing Git, it's essential to verify that the installation was successful.
  - This can be done by opening a terminal or command prompt and typing `git --version`. If Git is installed correctly, this command will display the installed version of Git.

### Git Setup (Configuration):
  - Before using Git, it's recommended to set up your user information such as name and email address.
  - This information is used to identify the author of commits within a repository.
  - Configuration can be done using the `git config` command, specifying the `--global` flag to set user information globally for all repositories, or omitting it to set information locally for a specific repository.

### SSH Keys Setup
  - SSH keys are used to securely authenticate your computer when communicating with remote servers.
  - To set up SSH keys for Git, you generate a key pair (public and private) using the `ssh-keygen` command.
  - Once generated, you add the public key to your Git hosting service (e.g., GitHub) to enable secure authentication when pushing and pulling from repositories.
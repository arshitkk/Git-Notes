# Git Cheatsheet

# Configuring user information
git config --global user.name "Your Name"          # Sets the name you want attached to your commit transactions
git config --global user.email "your.email@example.com" # Sets the email you want attached to your commit transactions

# Basic Git Commands
git init                                            # Initializes a new Git repository
git clone <repository>                              # Clones a repository into a new directory

# Making Changes
git status                                          # Shows the working directory status
git add <file>                                      # Adds a file to the staging area
git add .                                           # Adds all files in the current directory to the staging area
git commit -m "Commit message"                      # Records changes to the repository with a message

# Viewing History
git log                                             # Shows commit logs
git log --oneline                                   # Shows commit logs in a simplified form

# Branching
git branch                                          # Lists all local branches
git branch <branch-name>                            # Creates a new branch
git checkout <branch-name>                          # Switches to the specified branch
git checkout -b <branch-name>                       # Creates and switches to a new branch
git merge <branch-name>                             # Merges the specified branch into the current branch

# Remote Repositories
git remote add <name> <url>                         # Adds a remote repository
git remote -v                                       # Lists all configured remote repositories
git fetch <remote>                                  # Fetches changes from the remote repository
git pull <remote> <branch>                          # Fetches and merges changes from the remote branch
git push <remote> <branch>                          # Pushes changes to the remote branch

# Undoing Changes
git reset <file>                                    # Unstages a file
git reset --hard                                    # Resets the working directory to the last commit
git reset --hard <commit>                           # Resets the working directory and index to the specified commit
git revert <commit>                                 # Creates a new commit that undoes the changes from a previous commit

# Stashing
git stash                                           # Stashes changes in a dirty working directory
git stash list                                      # Lists all stashes
git stash apply                                     # Applies the latest stash
git stash apply stash@{n}                           # Applies the nth stash
git stash drop                                      # Deletes the latest stash
git stash drop stash@{n}                            # Deletes the nth stash

# Tagging
git tag                                              # Lists tags
git tag <tag-name>                                   # Creates a new tag
git tag -a <tag-name> -m "Tag message"               # Creates an annotated tag with a message
git push <remote> <tag-name>                         # Pushes a tag to the remote repository

# Viewing Differences
git diff                                             # Shows changes between working directory and index
git diff <commit>                                    # Shows changes between working directory and specified commit
git diff <commit1> <commit2>                         # Shows changes between two commits

# Rebase
git rebase <branch>                                  # Reapplies commits on top of another base tip
git rebase --continue                                # Continues rebase after resolving conflicts
git rebase --abort                                   # Aborts the rebase and returns to the original branch

# Cleaning
git clean -f                                         # Removes untracked files from the working directory
git clean -fd                                        # Removes untracked files and directories

# Working with Submodules
git submodule add <repository> <path>                # Adds a new submodule
git submodule update                                 # Initializes, fetches and checks out the submodule
git submodule init                                   # Initializes the submodule
git submodule deinit <path>                          # Deinitializes the submodule

# Gitignore
echo "pattern" >> .gitignore                         # Adds a pattern to the .gitignore file
git rm -r --cached .                                 # Removes all files from the index and stages them for a commit

# Useful Aliases
git config --global alias.st "status"                # Creates a shortcut for 'status'
git config --global alias.co "checkout"              # Creates a shortcut for 'checkout'
git config --global alias.br "branch"                # Creates a shortcut for 'branch'
git config --global alias.ci "commit"                # Creates a shortcut for 'commit'

# Git Help
git help <command>                                   # Shows help for a specific Git command


# For more detailed information, refer to the official Git documentation at https://git-scm.com/doc

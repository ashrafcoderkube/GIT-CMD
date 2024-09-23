# Git Commands Cheat Sheet

This document provides a comprehensive list of Git commands for version control. Git helps teams collaborate on projects by tracking changes in source code.

## Table of Contents

- [Basic Commands](#basic-commands)
- [Branching and Merging](#branching-and-merging)
- [Remote Repositories](#remote-repositories)
- [Tagging](#tagging)
- [Stashing](#stashing)
- [Undoing Changes](#undoing-changes)
- [Inspecting and Comparing](#inspecting-and-comparing)
- [Configuration](#configuration)
- [Collaboration](#collaboration)

---

## Basic Commands

- `git init`  
  Initializes a new Git repository in the current directory.

- `git clone [url]`  
  Clones an existing repository from a remote URL.  
  Example with a Personal Access Token (PAT):  
  ```bash
  git clone https://<PAT>@github.com/<username>/<repository>.git
  ```

- `git add [file]`  
  Adds changes in the specified file to the staging area.

- `git commit -m "[message]"`  
  Commits staged changes with a descriptive message.

- `git status`  
  Displays the status of the working directory and staging area, showing current branch and changes.

- `git log`  
  Shows the commit history for the repository.

- `git diff`  
  Displays the changes between the working directory and the staging area or between commits.

- `git reset [file]`  
  Unstages the specified file without modifying the working directory.

- `git rm [file]`  
  Removes the file from the working directory and stages the removal.

- `git mv [old_filename] [new_filename]`  
  Renames or moves a file and stages the change.

## Branching and Merging

- `git branch`  
  Lists all branches and shows the current branch with an asterisk (`*`).

- `git branch -d [branch_name]`  
  Deletes the specified branch.

- `git checkout [branch_name]`  
  Switches to the specified branch.

- `git checkout -b [branch_name]`  
  Creates and switches to a new branch.

- `git merge [branch_name]`  
  Merges the specified branch into the current branch.

- `git rebase [branch_name]`  
  Reapplies commits on top of another base branch to maintain a linear history.

## Remote Repositories

- `git remote add [name] [url]`  
  Adds a remote repository with the given name.

- `git remote -v`  
  Displays the URLs for the remote repository.

- `git fetch [remote_name]`  
  Fetches changes from the remote repository but doesn’t apply them.

- `git pull [remote_name] [branch_name]`  
  Fetches and integrates changes from the remote branch into the current branch.

- `git push [remote_name] [branch_name]`  
  Pushes local changes to the remote branch.

- `git push origin --delete [branch_name]`  
  Deletes a remote branch.

## Tagging

- `git tag [tag_name]`  
  Tags a specific commit with the given tag name.

- `git tag -a [tag_name] -m "[message]"`  
  Creates an annotated tag with a message.

- `git push [remote_name] [tag_name]`  
  Pushes the tag to the remote repository.

- `git tag -d [tag_name]`  
  Deletes the tag locally.

- `git push --delete [remote_name] [tag_name]`  
  Deletes the tag from the remote repository.

## Stashing

- `git stash`  
  Temporarily stores modified and staged changes for later use.

- `git stash pop`  
  Applies and removes the most recent stashed changes.

- `git stash apply`  
  Applies the most recent stash without removing it from the stash list.

- `git stash list`  
  Lists all stashed changes.

- `git stash drop`  
  Removes the most recent stash from the list without applying it.

- `git stash clear`  
  Clears all stashes.

## Undoing Changes

- `git revert [commit]`  
  Creates a new commit that undoes the changes from a specific commit.

- `git reset --hard [commit]`  
  Resets the current branch to the specified commit and discards all changes.

- `git reset --soft [commit]`  
  Resets the current branch to the specified commit but keeps the changes in the staging area.

- `git reset [commit]`  
  Moves the HEAD to the specified commit without discarding changes.

- `git checkout [file]`  
  Restores the specified file to the last committed state.

## Inspecting and Comparing

- `git show [commit]`  
  Displays the content and metadata of the specified commit.

- `git blame [file]`  
  Shows who modified each line of the file and when.

- `git log --oneline`  
  Displays the commit history in a compact format.

- `git diff [branch1] [branch2]`  
  Shows the difference between two branches.

- `git diff [commit] [file]`  
  Shows changes between a commit and the current state of a file.

## Configuration

- `git config --global user.name "[name]"`  
  Sets the username for all commits.

- `git config --global user.email "[email]"`  
  Sets the email address for all commits.

- `git config --list`  
  Lists all configuration settings.

- `git config --global alias.[alias_name] [git_command]`  
  Creates an alias for a Git command.

## Collaboration

- `git cherry-pick [commit]`  
  Applies a commit from another branch into the current branch.

- `git fetch --all`  
  Fetches changes from all remote repositories.

- `git pull --rebase`  
  Fetches changes and replays local commits on top of the pulled commits.

- `git push --force`  
  Force-pushes local changes to the remote repository, overwriting remote commits.

- `git pull origin master --allow-unrelated-histories`  
  Merges two unrelated histories from different repositories.

- `git pull [remote_name] --rebase`  
  Pulls changes and rebases your local changes on top of them.

---

## Cloning with a Personal Access Token (PAT)

To clone a repository using a Personal Access Token (PAT):

```bash
git clone https://<PAT>@github.com/<username>/<repository>.git
```

Replace `<PAT>` with your personal access token, `<username>` with your GitHub username, and `<repository>` with the repository name.

---

This cheat sheet covers the most frequently used Git commands. For more information or advanced usage, refer to the official [Git documentation](https://git-scm.com/doc).

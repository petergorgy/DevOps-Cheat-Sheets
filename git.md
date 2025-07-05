# GIT COMMANDS

## Table of Contents
- [GIT COMMANDS](#git-commands)
  - [Table of Contents](#table-of-contents)
  - [Configure tooling](#configure-tooling)
  - [Create repositories](#create-repositories)
  - [Branches](#branches)
  - [Create repositories](#create-repositories-1)
  - [Synchronize changes](#synchronize-changes)
  - [Make changes](#make-changes)
  - [Viewing the staged/unstaged changes](#viewing-the-stagedunstaged-changes)
  - [Redo commits](#redo-commits)
  - [The .gitignore file](#the-gitignore-file)
  - [GitHub Flow](#github-flow)
  - [Glossary](#glossary)

## Configure tooling

Configure user information for all local repositories

```
$ git config --global init.defaultBranch main
```

Sets the name you want attached to your commit transactions
```
$ git config --global user.name "Your Name"
```

Sets the email you want attached to your commit transactions
```
$ git config --global user.email "you@example.com"
```

Enables helpful colorization of command line output
```
$ git config --global color.ui auto
```

## Create repositories

When starting out with a new repository, you only need to do it once; either locally, then push to GitHub, or by cloning an existing repository.

Turn an existing directory into a git repository
```
$ git init
```

Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits
```
$ git clone [url]
```
## Branches

Branches are an important part of working with Git. Any commits you make will be made on the branch you're currently “checked out” to. 
Use `git status` to see which branch that is.

| COMMAND                       | DESCRIPTION                                                                                                                                |
| :---------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------- |
| $ git branch -c [branch-name] | Creates a new branch                                                                                                                       |
| $ git branch -a               | List all the branches                                                                                                                      |
| $ git checkout [branch-name]  | Switches to the specified branch and updates the working directory                                                                         |
| $ git merge [branch]          | Combines the specified branch’s history into the current branch. This is usually done in pull requests, but is an important Git operation. |
| $ git switch [branch-name]    | changing the current working branch to [branch-name], updating HEAD pointer and working directory to match that branch's state.            |
| $ git branch -d [branch-name] | Deletes the specified branch                                                                                                               |

## Create repositories

When starting out with a new repository, you only need to do it once; either locally, then push to GitHub, or by cloning an existing repository.

| COMMAND           | DESCRIPTION                                                                                                    |
| :---------------- | :------------------------------------------------------------------------------------------------------------- |
| $ git init        | Turn an existing directory into a git repository                                                               |
| $ git clone [url] | Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits |

## Synchronize changes

Synchronize your local repository with the remote repository on GitHub.com

| COMMAND                                  | DESCRIPTION                                                                                                                                                                                                             |
| :--------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $ git remote add origin [repository-url] | Establishes a connection between your local Git repository and a remote repository located at [repository-url], assigning it the conventional shortname "origin" for easy reference in subsequent push/pull operations. |
| $ git fetch                              | Downloads all history from the remote tracking branches.                                                                                                                                                                |
| $ git merge                              | Combines remote tracking branch into current local branch.                                                                                                                                                              |
| $ git push --all -uf origin main         | Force-pushes all local branches to their corresponding remote branches on the "origin" remote, overwriting any conflicting history on the remote, and explicitly targets the `main` branch if it's the current one.     |
| $ git pull                               | Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. `git pull` is a combination of `git fetch` and `git merge`.                                              |

## Make changes

Browse and inspect the evolution of project files

| COMMAND                                 | DESCRIPTION                                                                                                                                                       |
| :-------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $ git add [file]                        | Snapshots the file in preparation for versioning.                                                                                                                 |
| $ git add .                             | Snapshots all files in the directory in preparation for versioning.                                                                                               |
| $ git commit -m "[descriptive-message]" | Records file snapshots permanently in version history.                                                                                                            |
| $ git commit                            | Opens the default editor to type a long message.                                                                                                                  |
| $ git commit -am “Message”              | Skipping the staging area                                                                                                                                         |
| $ git rm [file-name]                    | Removes a file from both the Git staging area (index) and your working directory, preparing its deletion for the next commit.                                     |
| $ git rm --cached file1.js              | Removes from staging area only.                                                                                                                                   |
| $ git mv [file-name] [new-file-name]    | Renames or moves a file within your Git repository and automatically stages the change for commit, ensuring Git tracks the file's history across the rename/move. |

## Viewing the staged/unstaged changes

| COMMAND                                     | DESCRIPTION                                                   |
| :------------------------------------------ | :------------------------------------------------------------ |
| $ git diff                                  | Shows unstaged changes.                                       |
| $ git diff --staged                         | Shows staged changes.                                         |
| $ git diff --cached                         | Same as the above.                                            |
| $ git diff [first-branch]...[second-branch] | Shows content differences between two branches                |
| $ git log                                   | Lists version history for the current branch.                 |
| $ git log --oneline                         | Lists version history for the current branch in one line.     |
| $ git log --follow [file]                   | Lists version history for a file, including renames.          |
| $ git show [commit]                         | Outputs metadata and content changes of the specified commit. |
| $ git show HEAD                             | Shows the last commit.                                        |
| $ git show HEAD~2                           | Two steps before the last commit.                             |
| $ git show HEAD:[filename]                  | Shows the version of file.js stored in the last commit.       |

## Redo commits

Erase mistakes and craft replacement history.

| COMMAND                     | DESCRIPTION                                                    |
| :-------------------------- | :------------------------------------------------------------- |
| $ git reset [commit]        | Undoes all commits after [commit], preserving changes locally. |
| $ git reset --hard [commit] | Discards all history and changes back to the specified commit. |

## The .gitignore file

Sometimes it may be a good idea to exclude files from being tracked with Git. This is typically done in a special file named `.gitignore` . You can find helpful templates for `.gitignore` files at [github.com](https://github.com/github/gitignore).

## GitHub Flow
![GitHub Flow](img/github_flow.png "GitHub Flow")

## Glossary

* **git**: an open source, distributed version-control system 
* **GitHub**: a platform for hosting and collaborating on Git repositories 
* **commit**: a Git object, a snapshot of your entire repository compressed into a SHA 
* **branch**: a lightweight movable pointer to a commit 
* **clone**: a local version of a repository, including all commits and branches 
* **remote**: a common repository on GitHub that all team member use to exchange their changes 
* **fork**: a copy of a repository on GitHub owned by a different user 
* **pull request**: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more 
* **HEAD**: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git checkout
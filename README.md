# Git Commands

Git is a powerful and widely used version control system for software development. It allows developers to keep track of changes made to their code and collaborate with others on a project. Here are some common Git commands you'll use when working with a Git repository, along with the arguments and options they take:

## git init

This command is used to initialize a new Git repository. It creates a new directory with all the necessary files and folders for a Git repository, including the .git folder which contains all the information about the repository's history.

#### git init [directory]

    directory: The name of the directory where the new repository will be created. If no directory is specified, the current working directory will be used.

## git clone

This command is used to create a copy of an existing Git repository on your local machine. It allows you to download the entire repository, including all its branches and commits, and start working on it right away.

#### git clone [url] [directory]

    url: The URL of the remote repository you want to clone. This can be an HTTPS or SSH URL.
    directory: The name of the directory where the cloned repository will be created. If no directory is specified, the repository will be cloned into a directory with the same name as the repository.

## git add

This command is used to stage changes made to your files. When you make changes to a file in a Git repository, they are not automatically tracked by Git. You need to use the git add command to tell Git which changes you want to include in the next commit.

#### git add [file]

    file: The name of the file you want to stage. You can specify multiple files by separating them with spaces. If no file is specified, all changes in the working directory will be staged.

## git commit

This command is used to save changes to the Git repository. When you use the git commit command, you're creating a new "commit" in the repository's history. This commit includes all the changes that were staged using the git add command.

#### git commit -m "message"

    -m: The message flag, followed by a message in quotes, is used to specify a commit message. The commit message should be a brief, clear description of the changes made in the commit.

## git push

This command is used to upload changes made to your local repository to a remote repository, such as one hosted on GitHub. When you use the git push command, your commits are sent to the remote repository, where they can be shared with others.

#### git push [remote] [branch]

    remote: The name of the remote repository you want to push to. If no remote is specified, the default remote (usually origin) will be used.
    branch: The name of the branch you want to push. If no branch is specified, the current branch will be used.

## git pull

This command is used to download changes from a remote repository to your local repository. When you use the git pull command, Git will automatically merge any changes from the remote repository with your local repository.

#### git pull [remote] [branch]

    remote: The name of the remote repository you want to pull from.
    
    branch: The name of the branch you want to pull. If no branch is specified, the default branch (usually master) will be used.

## git status

This command is used to check the current status of your repository. It will show you which files have been modified, which changes have been staged, and which commits have been made. This command is useful for keeping track of the changes you've made and understanding the current state of your repository.

#### git status

This command takes no arguments.

## git branch

This command is used to manage branches in a Git repository. A branch is a separate line of development that allows you to work on different features or fix bugs in isolation. With git branch command, you can create, list, rename and delete branches.

#### git branch [branch_name]

    branch_name: The name of the branch you want to create. If no name is specified, all branches in the repository will be listed.

#### git branch -d [branch_name]

    -d: The delete flag, is used to delete a branch.
    branch_name: The name of the branch you want to delete.

#### git branch -m [old_branch_name] [new_branch_name]

    -m: The move flag, is used to rename a branch.
    old_branch_name: The current name of the branch you want to rename.
    new_branch_name: The new name of the branch.
    
## git checkout

The git checkout command is used to switch between different branches in a Git repository, or to restore files to a specific version.

#### git checkout [branch_name]

    branch_name: The name of the branch you want to switch to.

#### git checkout -b [new_branch_name]

    -b: The option to create a new branch and switch to it.
    new_branch_name: The name of the new branch you want to create.

#### git checkout [commit_id] -- [file_name]

    commit_id: The ID of the commit you want to restore the file to.
    --: The separator between the commit ID and the file name.
    file_name: The name of the file you want to restore.

#### git checkout -- [file_name]

    --: The option to discard changes to the file in the working directory.
    file_name: The name of the file you want to discard changes to.

It's important to note that when you switch to a different branch, git will update the files in the working directory to reflect the state of the files in the branch you switch to. And when you use git checkout to restore a file to a specific version, it will discard any changes you made to that file in the working directory. Make sure to save your work before using these commands.

## git merge

This command is used to combine the changes made in different branches. When you use the git merge command, Git will automatically combine the changes from one branch with another. This is useful when you want to bring changes from a feature branch into the main branch of the repository.

#### git merge [branch_name]

    branch_name: The name of the branch you want to merge. This should be the name of the branch that you want to bring changes from.

It is important to note that Git will automatically perform a merge only if it can be done without conflicts. If there are conflicts, you'll need to resolve them manually before the merge can be completed.

## git stash

This command is used to temporarily save changes that you have made in your working directory, but have not yet committed, to a new stash. This allows you to switch to a different branch or to return to a clean state without losing your changes.

#### git stash [name]

    name: The name of the stash. If no name is specified, a default name will be used.

#### git stash list

This command lists all the stashes that you have created.

#### git stash apply [name]

    name: The name of the stash you want to apply.

#### git stash drop [name]

    name: The name of the stash you want to delete.

## git log

This command is used to display the commit history of the repository. The log will show the commits in reverse chronological order, with the most recent commit at the top.

#### git log

This command takes no arguments and will show all the commits in the repository.

#### git log -n [number]

    -n: The number of commits to show.
    number: The number of commits you want to see.

#### git log --since=[date]

    --since: Show commits made after a specific date.
    date: The date you want to start showing commits from in the format "yyyy-mm-dd".

#### git log --author=[author]

    --author: Show commits made by a specific author.
    author: The name of the author you want to filter by.

## git diff

This command is used to see the differences between two versions of a file or between the working directory and the last commit. This command is useful for reviewing changes that have been made before committing them.

#### git diff

This command will show the differences between the working directory and the last commit.

#### git diff [file]

    file: The name of the file you want to see the differences of.

#### git diff [branch1] [branch2]

    branch1: The name of the first branch you want to compare.
    branch2: The name of the second branch you want to compare.

#### git diff [commit1] [commit2]

    commit1: The first commit you want to compare.
    commit2: The second commit you want to compare.

## git reset

This command is used to undo commits and change the state of the repository. It allows you to move the head pointer and change the contents of the working directory.

## git reset [commit]

    commit: The commit you want to reset to.

## git reset --hard

    --hard: This option discards all changes in the working directory and resets the repository to the specified commit.

## git reset --soft

    --soft: This option keeps the changes in the working directory and undoes the specified commit.

It is important to use this command with caution, as it can permanently delete commits and changes.

These are some of the most commonly used Git commands, along with the arguments and options they take. Remember that Git is a powerful tool and it takes practice and experience to master it. Always make sure to read the documentation and understand the consequences of each command before using them.

_________________________________________________



## git fetch

This command is used to download commits, files, and refs from a remote repository to your local repository without merging them. This command is useful for getting the latest changes from a remote repository without affecting your local branches.

#### git fetch [remote]

    remote: The name of the remote repository you want to fetch from. If no remote is specified, the default remote (usually origin) will be used.

#### git fetch [remote] [branch]

    remote: The name of the remote repository you want to fetch from.
    branch: The name of the branch you want to fetch.

#### git fetch --all

    --all: This option fetches from all remotes.

## git rebase

This command is used to reapply commits on top of another branch. It allows you to incorporate new changes from a branch into your current branch. This command is useful for keeping your branch up to date with the latest changes from the upstream branch.

#### git rebase [branch]

    branch: The name of the branch you want to rebase onto.

#### git rebase --onto [newbase] [branch1] [branch2]

    --onto: The option to specify the new base for the rebase.
    newbase: The new base commit for the rebase.
    branch1: The branch you want to rebase.
    branch2: The branch you want to rebase onto.

It is important to note that Git will automatically perform a rebase only if it can be done without conflicts. If there are conflicts, you'll need to resolve them manually before the rebase can be completed. Also, Rebase can also be dangerous as it rewrites the commit history, so use it carefully.

## git tag

This command is used to create, list, and delete tags in a Git repository. A tag is a named reference to a specific commit, and it's often used to mark important versions or milestones in the development of a project.

#### git tag [tag_name]

    tag_name: The name of the tag you want to create.

#### git tag

This command lists all the tags in the repository.

#### git tag -d [tag_name]

    -d: The delete flag is used to delete a tag.
    tag_name: The name of the tag you want to delete.

#### git tag -a [tag_name] -m "message"

    -a: The annotation flag is used to create an annotated tag.
    tag_name: The name of the tag you want to create.
    -m: The message flag, followed by a message in quotes, is used to specify a message for the tag.

#### git tag -f [tag_name]

    -f: The force flag is used to move an existing tag to a new commit.
    tag_name: The name of the tag you want to move.

## git cherry-pick

This command is used to apply specific commits from one branch to another branch. It allows you to select individual commits and apply them to a different branch, rather than merging an entire branch.

#### git cherry-pick [commit]

    commit: The commit you want to apply.

It is important to note that Git will automatically perform a cherry-pick only if it can be done without conflicts. If there are conflicts, you'll need to resolve them manually before the cherry-pick can be completed.

## git remote

This command is used to manage remote repositories in a Git repository. Remote repositories are other copies of the repository, that you can push and pull changes from.
git remote

This command lists all the remote repositories that you have configured in your local repository.
git remote add [remote_name] [remote_url]

    remote_name: The name you want to give to the remote repository.
    remote_url: The URL of the remote repository you want to add.

#### git remote remove [remote_name]

    remote_name: The name of the remote repository you want to remove.

#### git remote rename [old_name] [new_name]

    old_name: The current name of the remote repository.
    new_name: The new name you want to give to the remote repository.

#### git remote set-url [remote_name] [new_url]

    remote_name: The name of the remote repository you want to update.
    new_url: The new URL you want to set for the remote repository.

## git archive

This command is used to create an archive file of a specific commit, branch, or tag in your repository. The archive file can be in different formats such as zip, tar, or gzip. This command is useful for creating backups or for distributing a specific version of your project.
git archive [commit/branch/tag]

    commit/branch/tag: The name of the commit, branch, or tag you want to archive.

#### git archive --format=[format] [commit/branch/tag] -o [filename]

    --format: The format of the archive file.
    format: The format of the archive file, such as zip, tar, gzip.
    commit/branch/tag: The name of the commit, branch, or tag you want to archive.
    -o: The output file flag, followed by the desired filename, where the archive will be saved.

## git submodule

This command is used to manage submodules in a Git repository. Submodules are additional Git repositories that are included in the main repository. This allows you to use code from other projects as a part of your own project, while still keeping them separate and maintainable.

#### git submodule add [remote_url] [path]

    remote_url: The URL of the submodule repository you want to add.
    path: The directory where the submodule repository will be added in your main repository.

#### git submodule init

This command initializes submodules in the local repository.

#### git submodule update

This command updates the submodules in the local repository.

#### git submodule status

This command shows the status of the submodules in the local repository.

#### git submodule deinit [path]

    path: The path of the submodule you want to remove.

#### git submodule foreach [command]

    command: The command you want to run for each submodule.

It is important to note that the submodule command set is relatively complex, so it's important to understand the implications of each command before using them, and to use them with caution. Remember to always backup your work before doing anything destructive and to consult the official documentation.

These are some of the Git commands related to submodules, they allow you to manage and include other Git repositories as a part of your own project, while still keeping them separate and maintainable.

These are some more advanced Git commands that can be useful in certain situations. It's important to understand the implications of each command before using them, and to use them with caution. Git is a powerful tool and it takes practice and experience to master it. Remember to always backup your work before doing anything destructive and to consult the official documentation.

__________________________________________________

# Git_Github_notes

 ![logo](docs/f6d.png)

## Git and Github notes

### First steps

- To install git on ubuntu
  ```
  $ sudo apt-get update
  $ sudo apt-get install git 
  ```
- To configure user information for all local repositorie
    ```
    $ git config --global user.name "[your_name]"
    ```

    > allows you to sets the name attached to your commits transactions

    ```
    $ git config --global user.email "[email address]"
    ```

    > Sets the email    attached to your commits transactions

### Create Repo

A new repository can either be created
locally, or an existing repository can be cloned. When a repository was initialized locally, you have to push it to GitHub afterwards.
```
$ git init
```

>Set the directory you are in as git repository


  After using the ***git init command*** , link the local repository to an empty GitHub repository using the following command:
  ```
  $ git remote add origin [url]
  ```
  >The url points to a repository on GitHub
```
$ git clone [url]
```
> Clone (download) a repository on Github with all files,branches and commits.

## Sync is life 

Let's get some data for our local repository

```
$ git fetch 
```
>Downloads all history from the remote tracking branches

```
$ git merge
```
>Combines remote tracking branches into current local branch

```
$ git push
```

> Uploads all local branch commits to Github

```
$ git pull
```

> Update your current local working branch with all new commits from the corresponding remote branch on GitHub

## A tree without branches is not a tree

- Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to. Use git status to see which branch that is.

```
$ git branch [branch-name]
```

>Create a new branch

```
$ git switch -c [branch-name]
```

> Switches to the specified branch and updates the woring directory 

```
$ git merge [branch]
```

> Combines the specified branch's history into the current branch. This is usually done in pull requests, but is an important Git operation.

```
$ git branch -d [branch-name]
```

> Deletes the specified branch

## History is a better guide than good intentions

If u need to browse and inspect the evolution of project files

```
$ git log
```

> Lists version history for current branch

```
$ git log --follow [file]
```

> Lists version history for a file, beyond renames (only for a single file)

```
$ git diff [first-branch]...[second-branch]
```

> Shows content differences between two branches

```
git show [commit]
```

> Outputs metadata and content changes of the specified commit

```
git add [file]
```
> Snapshots the file in preparation for versioning 

```
$ git commit -m "[descriptive message]"
```

> Records files snapshots permanently in version history

## An error can be undone

if u made a mistake erase it and craft replacement history 

```
$ git reset [commit]
```

> Undoes all commits after [commit], preserving changes locally

```
$ git reset --hard [commit]
```

> Discards all hsitory and changes back to the specified commit


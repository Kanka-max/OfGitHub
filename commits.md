## Creating and editing commits / Pull Requests / Merge Conflicts

### About Commits
A commit records changes to one/more files in your branch.
Git assigns each commit a uniqueID, SHA, hash, that identifies:
- The specific changes.
- When the changes were made.
- Who created the changes.

Include a commit message that briefly describes the changes.
#### Create commit with multiple authors.
- Attribute a commit to more than one author.
- Add one or more **Co-authored-by** trailers to the commit message.
##### Required co-author information
- Know the appropriate email to use for each co-author.
- Use email associated with their GitHub Acc.
- If a person chooses to keep their email address private;
- Use their email provide *no-reply* to provide privacy.
- If you want to keep your email private;
- Choose to use GitHub-provided *no-reply* email for Git operations.
- Ask co-authors to list your *no-reply* email in commit trailers.
- To find the email you used to configure Git on your computer, run **git config user.email** on the command line.

[Command Line](https://docs.github.com/en/github/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)

### Pull Requests
### About Forks
Forks - copy of repo that you manage.
You can fetch updates from or submit changes to the original repo with pull requests.
- Pull request to suggest changes to from your user-owned fork to your original repo; *upstream repository*.
- Bring changes from the upstream repository to your local fork by synchronizing your fork with the *upstream repository*.
- In open-source; forks are often used to iterate on ideas or changes before they are offered back to the *upstream repository*.
- When you make changes in your user-owned and open a pull request that compares your work to the *upstream repository*;
- You can give anyone push access to the upstream repo permission to push changes to your pull request branch.
- Speeds up collaboration by;
- Allowing repo maintainers the ability to make changes commits or run tests locally to your pull request branch from a user-owned fork before merging.

- You cannot give push permissions to a fork owned by an organization.
- Private forks inherit the permissions structure of the upstream/parent repo.
- Creating a new repo from the contents of an existing repo; without merging your changes upstream;
- Duplicate the repo; 
- If repo is a template, use repo as template.

### Configuring a remote for a fork
- Configure a remote that points to the upstream repository.
- To sync changes you make in a fork with the original repo.

1. Open Git Bash
2. List the current configured remote repository for your fork.
  ```
 $ git remote -v
> origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
> origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
```

3. Specify a new remote *upstream* repo that will be synced with the fork.
  ```
  $ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
  ```
  
4. Verify the new *upstream* you've specified for your fork.
  ```
 $ git remote -v
> origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
> origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
> upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
> upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
  ```
  
### Syncing a fork
- Sync a fork repo to keep up-to-date with the upstream repo.
- Before syncing a forked repo to your upstream repo
- Configure a remote that points to the upstream repo.

1. Open Git Bash.
2. Change your current working DIR to your local project.
3. Fetch the branches, and their respective commits from the upstream repo.
  - Commits to a **BRANCHNAME** will be stored in the local branch **upstream/BRANCHNAME**.

```
$ git fetch upstream
> remote: Counting objects: 75, done.
> remote: Compressing objects: 100% (53/53), done.
> remote: Total 62 (delta 27), reused 44 (delta 9)
> Unpacking objects: 100% (62/62), done.
> From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
>  * [new branch]      main     -> upstream/main
```

4. Check your fork's local default branch (main in this case)
```
$ git checkout main
> Switched to branch 'main'
```

5. Merge the changes from the upstream default branch (*upstream/main*) into your local default branch.
*Brings your fork's default branch into sync with the upstream repository/ without losing your local changes.*

```
$ git merge upstream/main
> Updating a422352..5fdff0f
> Fast-forward
>  README                    |    9 -------
>  README.md                 |    7 ++++++
>  2 files changed, 7 insertions(+), 9 deletions(-)
>  delete mode 100644 README
>  create mode 100644 README.md
```

*If your local branch didn't have any commits, Git will instead perform a **fast-foward**.

```
$ git merge upstream/main
> Updating 34e91da..16c56ad
> Fast-forward
>  README.md                 |    5 +++--
>  1 file changed, 3 insertions(+), 2 deletions(-)
```

- Syncing your fork only updates your local copy of the repo;
- To update your fork on GitHub, push your changes.

### Merging an upstream repository into your fork.
- If you don't have push(write) access to an upstream repo;
- Pull commits from that repo into your your own fork.
1. Open Git Bash.
2. Change working DIR to your local project directory.
3. Check out the branch you wish to merge (usually main/default)
```
$ git checkout DEFAULT_BRANCH_NAME
```
4. Pulled the desired branch from the upstream repo. Will retain commit history with no modifications. 
```
$ git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME
```
5. Address any merge conflicts.
6. Commit the merge.
7. Review changes and make sure they are satisfactory.
8. Push the merge to your GitHub Repo.

### Addressing Merge Conflicts

If you have merge conflicts with the base branch;
You MUST address them before you can merge your pull request's changes.

### About Merge Conflicts
- Happens when;
- You merge branches that have competing commits.
- Decide which changes to incorporate in the final merge.
- Git can resolves this automatically;
- Usually changes are on different lines/ different files.
- Often happen when people make different changes to same line of the same file; or
- One person edits a file and another deletes the file.
- Merge conflict between compare branch/ base branch in your pull request;
- View a list of the files with conflicting changes above the **Merge pull request** button.
- This button is deactivated until all conflicts are resolved.

### Resolving Merge Conflicts
You must manually edit the conflicted file to select the changes that you want to keep in your final merge.
- Merge conflict caused by competing line changes; 
  - When people make different changes to the same line in the same file on different branches in your Git repo;
  - Resolve it on GitHub on using conflict editor.
- All other types of conflicts.
  - Resolve in a local clone of the repo.
  - Push change to your branch in GitHub.

- If you have merge conflict on the command line;
- You can push your local changes to your GitHub until you resolve the merge conflict locally.
- If you try;
  ```
$ git merge BRANCH-NAME
> Auto-merging styleguide.md
> CONFLICT (content): Merge conflict in styleguide.md
> Automatic merge failed; fix conflicts and then commit the result

```

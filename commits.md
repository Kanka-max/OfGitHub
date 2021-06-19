## Creating and editing commits / Pull Requests

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

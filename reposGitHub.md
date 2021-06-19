## About Repos

### About Code Owners
- CODEOWNERS file defines individuals/teams that are responsible for code in repository.
- Have admin/owner permissionscan set up this file in the repo.
- When code owner is a team;
- Team must have read/write permissions for the repo.
- Code owners are automatically asked for review when someone opens a pull request that modifies the code they own.

### CODEOWNERS file location
- Create a new file: CODEWONERS in the root, *docs/* , or *.github/* of the repo.
- In the branch where you'd like to add the file.
- Each CODEOWNER file assigns assigns the code owners for a single branch in the repo.
- You can assign different code owners for different branches.
- For codeowners to receive requests;
- The CODEOWNERS file must be on the base branch of the pull request.

### CODEOWNERS Sytanx
- Pattern follows most of the *gitignore* rules with some **exceptions**.
- Pattern followed by one/more GitHub usernames/team names using the standard;
- **@username**/ **@org/team-name** format.
- If any line contains syntax issues;
- File will not be detected and will not be used to request reviews. 

## Licensing a Repo
- For a repo to be truly open-source;
- License it so others are free to use, change and distribute software.
- Software license tells others what they can and can't do.
- You're under obligation to choose a license.
- Without a license, default copyright always applies.
- You retain all rights to your source code and NO ONE can;
- Reproduce, distribute, or create derivative works from your works.

### Determining location of your license.
- In the root of your repo.
- *license.txt*, *license.md*, *license.rst*
- Project can include information about the license in the README.md file
- "This project is licensed under the terms of DESTINA license."
[Non Software Licences](https://choosealicense.com/non-software/)
[License](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/licensing-a-repository)

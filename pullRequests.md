## Reviewing Changes in Pull Requests
Reviews allow collaborators to comment on the changes proposed in pull requests; approve changes; request further changes; before merge.
Repo admins can require that all pull requests are approved before being merged.

### About Pull Request Reviews
- After a pull request is opened, anyone can with *read* access can review and comment on the changes it proposes.
- Suggest specific changes in line of codes, which the author can apply directly from the pull request.
- Repo owners and collaborators can request a pull request review from a specific person.
- Organization members can also a pull request review from a team with *read* access to repository;
- You can also specify a subset of team members to be automatically assigned in place of the whole team.

- Reviews allow for discussion of proposed changes and;
- Help ensure the changes meet the repository's contributing guidelines and other quality standards.
- When a pull request modifies code that has a defined owner;
- That individual/team will automatically be requested as a reviewer.

A review has these possible statuses:
- **Comment**: Submit general feedback without explicitly approving the changes/ requesting additional changes.
- **Approve**: Submit feedback and approve merging the changes proposed in the pull request.
- **Request Changes**: Submit feedback that must be addressed before the pull request can be merged.

#### TIPS
- If required reviews are enabled and a collaborator with *write*, *admin*, *owner* access to the repo submits a review requesting changes;
  - the pull request cannot be merged until the same collaborator submits another review approving the changes in the pull request.
- Repo owners and admins can merge a pull request even if it hasn't received an approving review;
  - or if a reviewer who requested changes has the left the organization or is unavailable.
- If both required reviews and stale review dismissal are enabled and a code-modifying is pushed to the branch of an approved pull request; approval is dismissed.
  - Pull request must be reviewed and approved again before it can be merged.
- When several open pull requests each have a head branch pointing to the same commit;
  - you won't be able to merge them if one or both have a pending/ rejected review.
- Pull request authors cannot approve their own pull requests.

View all of the reviews a pull request has received in the **Conversation Timeline**.
Repository administrators can require that all pull requests receive a specific number of approved reviews;
Before someone merges the pull request to a protected branch.

[pull requests](https://docs.github.com/en/github/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)




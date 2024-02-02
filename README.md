# Github Foundations Certification Study Guide

### Basic Function

### Types of Accounts

### GitHub Repos
> Repo Stats are tracked through Repo insights

<ins>Types of Repo Insights</ins>
- **Pulse** : Overview of recent activity (pull requests, issues)
- **Contributors** : Displays activity stats base on contributors
- **Community Standards** : Shows community health files
- **Commits** : History of all commits of repo
- **Code Frequency** :  Charts addtions and deletions over time
- **Dependency Graph** : Illustrates code dependencies
- **Network** : Shows fork relationships and variations
- **Forks** : Number and links to repo forks

### GitHub Issues

> Up to three issues can be pinned to a repo.

_Difference Between Actions_

- __Issues__ : Are for tracking tasks, bugs, and enhancements
    - usually linked to code changes
    - can be linked to Pull Requests

- __Discussions__ : For communication and Q & A
    - by topic
    - can be converted to issue (soft link)
    - Not directly related to code changes

- __Pull Requests__ : Proposing, reviewing and merging code changes
    - Can be linked to Issues
 
__To Link Issues__

- Open developement tab (right column); issues and branches will be linked by number.


 ##### Using Keywords in Issues & Pull Requests
To link a pull request to an issue to show that a fix is in progress and to automatically close the issue when         someone merges the pull requests. Use Keyword followed by the issue (example `closes #10`)

<ins>Keywords</ins>
- close
- closes
- closed
- fix
- fixes
- fixed
- resolve
- resolves
- resolved

#### Ways to Filter Issues

Issues can be displayed on issue dashboard. To find a specific issue search by:
- Open Issues
- Your Issues
- Your Pull Requests
- Everything assigned to You
- Everything mentioning You
- View advanced search syntax

```bash
# THIS IS advanced search syntax
is:issue author:username label:bug
is:issue label:bug label:urgent state:open 
is:issue assignee:username milestone:"v1.0"
is:issue no:assignee repo:username/repository comments:>=10
is:issue created:>=2022-01-01 created:<=2022-12-31
is:issue involves:username comments:0
is:issue language:python updated:>2022-01-01
```

[Complete Advanced Search Commands](https://docs.github.com/en/search-github/searching-on-github/searching-issues-and-pull-requests)

__Issue Templates__

It is possible to create issue templates, to help ensure all relevant information is included with new issues.
Issue Templates are <ins>stored as markdown files in</ins>  **.github/ISSUE_TEMPLATES** folder in the repo.

<ins>__3 Default GitHub issue templates__</ins>
- Bug Report
- Feature Report
- Report a security vulnerability

Here is the documentation [Link](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates) on how to create and use issue templates.

__Issue Forms__ (Beta)

*evolution of issue templates*

- YAML formatted file to create issue form for stricter entry of issue information.

### GitHub Pull Requests

> A Pull Request (PR) is a formal process to put forth changes, that can be manually or automatically reviewed before its accepted into the code base main branch.

<ins>Benefits of Pull Requests (Not unique to GitHub) </ins>
1. Collaborative Review: enhances code quality through team discussion.
2. Change Tracking: Provides record of code changes and related discussions.
3. Automated Testing: Enables CI/CD integration tools
4. Controlled Integration: Manages safe and reviewed merging of code changes
5. Open Source Friendly: Simplifies contributions and collaboration in open-source projects.

Ways to Create PR
- In GitHub repo, green New Pull Request button, then Create pull request
- In GitHub CLI, example create PR from a branch (below)
  
  ```bash
  git checkout -b new-feature-branch
  git commit -am "My commit message"
  git push -u origin new-feature-branch
  gh pr create --base main --head new-feature-branch
  ```

  #### Pull Request Statuses

  - Open : Default when PR is created
  - Draft : PR is work-in-progress, not yet ready for review
  - Closed : PR closed without being merged, when changes no longer needed
  - Merged : Successful adding to target branch
  - Changes Requested : Used during review process, before merged
  - Review Required : When mandatory reviews are part of workflow
  - Approved : When PR has been reviewed and approved by required number of reviewers.
  - Conflict : requesting branch and target branch need conflicts resolved before review
  - Ready for Review : Initial requests marked as drafts can be changed to this status when ready.

  #### Base and Compare
  > This determines the direction of the merge for a pull request

  - __Base__ is where you want to merge into (usually main branch)
  - __Compare__ is what (normally feature branch) will be merged into Base (this chooses Head reference)

    - Compare across forks
      > This checks two branch for what changed or starts new pull request.

#### Draft Pull Request (*Only on Organizations Teams*)
> Note for test; 1) these cannot be merged 2) code owners not automatically requested to review

<ins>Use Case for Draft Pull Requests</ins>
1. Indicates work-in-progree (WIP)
2. Prevents Premature Merging
3. Facilitates Early Feedback and Collaboration
4. COntinuous Integration Testing
5. Transitioning to a Ready State
6. Organiaing Work and Priorities

#### Merging a Pull Request Options
1. Create a merge commit : All commits will be added
2. Squash and merge : 1 commit will be added
3. Rebase and merge : 1 commit will be added and rebased

#### Pull Request Review
- Required Reviewers can be set to approve any PR
- Reviewers can make comments about PR and require addition changes
- Comments CAN be made on <ins>single line of code</ins> 


## Codespaces
> Cloud Developer Environment (CDE) integrated with your GitHub repo

__Interact with codespaces through:__
- Command Line (SSH via GitHub CLI)
- Code Editors
      - VS Code Browser & Desktop
      - JetBrains IDE

__When new Codespace is created choose__
- Repo
- Branch
- Region
- Machine Type

__Codespace Lifecycle__
- Create/Reopen
- Running
- Timeout
- Stop


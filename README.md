# Github Foundations Certification Study Guide

### Basic Function

### Types of Accounts

### GitHub Repos

##### Repo Insights

Types of Insights
- **Pulse** : Overview of recent activity (pull requests, issues)
- **Contributors** : Displays activity stats base on contributors
- **Community Standards** : Shows community health files
- **Commits** : History of all commits of repo
- **Code Frequency** :  Charts addtions and deletions over time
- **Dependency Graph** : Illustrates code dependencies
- **Network** : Shows fork relationships and variations
- **Forks** : Number and links to repo forks

### GitHub Issues

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






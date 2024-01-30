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

Keywords
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





# name of repo-newIssue
#-----CODE BELOW-------
#ISSUE URL-https://github.com/AlwaysLearner29/newIssue/issues
from github import Github
import os
from pprint import pprint
#CodeforCause Assignment
#NAME-Aryaman college-GBPEC btech CSE 1st yr.
#OPENING THE ISSUE USING Github libary.
#commented on newly created issue using githubAPI
token = os.getenv('GITHUB_TOKEN', '2b303633d9e979f88c0bfecfcd4092f3eacfee04')
g = Github(token)
repo = g.get_repo("AlwaysLearner29/newIssue")
i = repo.create_issue(
    title="first issue code for cause",
    body="new issue created",
    assignee="AlwaysLearner29",
    labels=[
        repo.get_label("good first issue")
    ]
)
pprint(i)
#I dont know how to close issue using Github API.

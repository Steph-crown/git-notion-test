name: Issue Automation
on:
issues:
types: [opened, edited, reopened]
jobs:
add-to-project-board:
name: Add issue to project board
runs-on: ubuntu-latest
steps: - name: Add new issues to project board
uses: matmar10/add-issues-to-project@master
with:
gitub_token: ${{ secrets.TOKEN }}
github_project_title: my-project
github_org: steph-crown

name: Add bugs to bugs project

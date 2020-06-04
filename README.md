# Task List Zero GitHub Action

This action checks if the tasks (checkboxes) listed inside the PR description are all checked and fails if that's not the case.

# How to add

```
- uses: adriferracuti/gha-task-list-zero@2.0
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

For example:

```
name: PR Metadata
on:
  pull_request:
    types: [opened, edited, synchronize, reopened]

jobs:
  comment:
    name: Comments checks
    runs-on: ubuntu-18.04
    steps:
      - uses: adriferracuti/gha-task-list-zero@dev-0.2
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
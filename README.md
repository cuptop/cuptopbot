# Gitbo

this is a telegram bot notify us about GitHub commits & push

add this into your github-workflow
```

name: <workflowname>

on:
  push:
  pull_request:
    types: [opened, closed]
  issues:
    types: [opened, closed, reopened]
jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: cuptopbot
        uses: cuptop/cuptopbot@master
        if: always()
        with:
          chat: ${{ secrets.chat }}
          token: ${{ secrets.token }}
          status: ${{ job.status }}

          
```

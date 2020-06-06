# bot

```

name: <your workflow name>

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
      - name: <name>
        uses: <user>/<repo name>@master
        if: always()
        with:
          chat: ${{ secrets.chat }}
          token: ${{ secrets.token }}
          status: ${{ job.status }}
          
```

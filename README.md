# first-demo-action
name: learn github-actions
on: [push]
jobs:
  check-bats-version
    runs-on: powershell
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
      - run: npm install -g bats
      - run: bats -v

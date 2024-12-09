# Update README CLI Action

This GitHub Action updates the README file with the usage section generated from the CLI.

## Usage

To use this action, create a workflow file (e.g., `.github/workflows/update-readme.yml`) in your repository with the following content:

```yaml
name: Update README CLI 

on:
  push:
    branches:
      - main

jobs:
  update-readme:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Use Update README Action
      uses: your-username/update-readme-cli-action@v1
      with:
        cli-path: './bin/cli.js'

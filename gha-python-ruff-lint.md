# How to setup a Ruff Python lint job on Git repo push
1. Create a new ".github" directory in your local repo
2. Create a new "workflows" directory within your .github directory
3. Create a "ruff-ci.yaml" file in your workflows directory
4. Paste in the following .yaml text in your ruff-ci.yaml file:
```
name: Ruff-CI

on:
  push:
  pull_request:

jobs:
  run-tests:
    strategy:
      fail-fast: false
      matrix:
        os: [ubuntu-latest, macos-latest, windows-latest]
        python-version:
          - "3.11"
        
    name: Ruff Lint
    runs-on: ${{ matrix.os }}

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Setup Python
        uses: actions/setup-python@v4
        with:
          python-version: ${{ matrix.python-version }}

      - name: Install Ruff
        run: python -m pip install ruff

      - name: Run Ruff
        run: python -m ruff check .        
```

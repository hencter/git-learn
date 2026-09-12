# GitHub CLI Quick Start

GitHub CLI (`gh`) is the official command-line tool for working with GitHub from a terminal. It helps you authenticate, create repositories, manage pull requests and issues, and inspect GitHub state without opening the browser for every step.

## Check Installation

```powershell
gh --version
```

## Sign In

```powershell
gh auth login
```

Follow the prompts to choose GitHub.com, HTTPS or SSH, and browser-based authentication.

## Common Commands

```powershell
# View current authentication status
gh auth status

# Create a new GitHub repository from the current folder
gh repo create

# Clone a repository
gh repo clone owner/repo

# View pull requests
gh pr list

# Create a pull request
gh pr create

# View issues
gh issue list

# Open the current repository in the browser
gh browse
```

## Typical Git Workflow With GitHub CLI

```powershell
git status
git add README.md
git commit -m "Add GitHub CLI quick start"
gh repo create --source . --remote origin --push
```

Use `gh help` or `gh <command> --help` to see more details for any command.

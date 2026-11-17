# DBS Devs – organization settings

This repository contains the shared rules and templates for all DBS Devs repositories.

| File | Purpose |
|---|---|
| `CONTRIBUTING.md` | Team rules: workflow, naming, pull requests, Jira |
| `pull_request_template.md` | Default pull request template for every repository |
| `workflow-templates/` | GitHub Actions ready to be added to a repository (e.g. Jira link) |
| `CODEOWNERS` | Reference template for automatic reviewers. Copy it to `.github/CODEOWNERS` in each repository and fill in areas and leads |

Start from [CONTRIBUTING.md](CONTRIBUTING.md).

## Starting a new app

Always create new repositories from `app-template`: it already includes
the pull request template and the Jira link Action.
A repository created with `git init` does **not** include them.

### Option 1 – Terminal (GitHub CLI)
Requires [GitHub CLI](https://cli.github.com/) and a one-time `gh auth login`.

Create the repository and clone it:

```bash
gh repo create DBS-Devs-Team/<app-name> --template DBS-Devs-Team/app-template --private --clone
```

Apply the repository settings (they are not copied from the template):

```bash
gh repo edit DBS-Devs-Team/<app-name> --delete-branch-on-merge
```

### Option 2 – GitHub website
1. Open [app-template](https://github.com/DBS-Devs-Team/app-template)
   and click **Use this template → Create a new repository**.
2. Owner: `DBS-Devs-Team`, name: `<app-name>`, visibility: **Private**.
3. Clone it:

```bash
git clone https://github.com/DBS-Devs-Team/<app-name>.git
```

4. Settings → General → Pull Requests: enable **Automatically delete head branches**.

Then follow the checklist in the app-template README.

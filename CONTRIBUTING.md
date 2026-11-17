# Contributing to DBS Devs

These rules apply to every repository in the organization.

## Workflow

1. Every piece of work starts from a **Jira task**.
2. Create a **branch** from `main` (see naming below).
3. Commit your changes (see naming below).
4. Open a **pull request** towards `main` and fill in the template.
5. Another team member **reviews** the pull request.
   With the GitHub Free plan the review cannot be enforced on private repositories
   (GitHub does not block the merge), so this is a team agreement.
6. After approval, merge the pull request into `main`.

**Never push directly to `main`.**

## Naming: branches and commits

Branches and commit messages follow the same rule: the **Jira task key**.

```
<JIRAKEY>-<number>
```

- `JIRAKEY` is the short code of the app's Jira project.
  Example: the project for the stats app has the key `APPSTATS`.
- `number` is the number of the task in that project, assigned automatically by Jira.
  Example: the 12th task of the stats app is `APPSTATS-12`.

| | Example |
|---|---|
| Branch | `APPSTATS-12` |
| Commit message | `APPSTATS-12` (optionally followed by a short description) |

- Jira links branches, commits and pull requests to the task automatically,
  as long as they contain the task key.
- **One task = one branch = one pull request.**
- Follow-up fixes on a task that is already merged: use a suffix
  (`APPSTATS-12-1`, `APPSTATS-12-2`…) and move the task back to *In progress*.
- New work: create a new Jira task.
- Be careful with the dash: `APPSTATS-12-1` is task 12 (fix 1),
  `APPSTATS-121` is a different task.
- The type of work (feature, bug fix…) is defined in the Jira task.
- The description of the change goes in the pull request template.

## Pull requests

### Opening a pull request
- Each pull request covers **one Jira task** only.
- Under **Jira task**, write the task key (e.g. `APPSTATS-12`).
- Fill in every section of the template. If a section does not apply, write `N/A`.

### Review
- Before merging, **another team member must review and approve** the pull request.
- You cannot approve your own pull

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
| Commit message | `APPSTATS-12` |

- The type of work (feature, bug fix…) is defined in the Jira task.
- The description of the change goes in the pull request template.

## Pull requests

### Opening a pull request
- Each pull request covers **one Jira task** only.
- Fill in every section of the template. If a section does not apply, write `N/A`.

### Review
- Before merging, **another team member must review and approve** the pull request.
- You cannot approve your own pull request.

### After the merge
- The branch is **deleted automatically** once the pull request is merged.
- Nothing is lost: the code is already on `main`, and the branch can be restored
  with the **Restore branch** button in the pull request.

## Open points

- **Merge strategy: squash or merge commit**
  *Squash and merge* combines all the commits of a pull request into a single commit on `main`,
  so `main` has one clean commit per task. *Merge commit* keeps every commit of the branch
  plus an extra merge commit. Since commit messages contain only the Jira key,
  squash is recommended: otherwise `main` would show several identical commit messages.
- **Areas and reviewers**: how to split the project areas and who is the lead reviewer
  for each one (CODEOWNERS).
- **Jira integration**: GitHub Action that automatically adds the Jira link to the
  pull request (when Jira is set up).
- **Visibility of the `.github` repository**: public or private.

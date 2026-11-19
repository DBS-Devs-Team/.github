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

Exception: the initial setup of a new repository (README, `.gitignore`, `CLAUDE.md`)
can be done directly on `main`, before work on tasks starts.

## Naming: branches, commits and pull requests

Branches, commit messages and pull request titles all use the **Jira task key**.

```
<JIRAKEY>-<number>
```

- `JIRAKEY` is the short code of the app's Jira project.
  Example: the stats app uses the key `DBS`.
- `number` is the number of the task in that project, assigned automatically by Jira.
  Example: task 12 of the stats app is `DBS-12`.

| | Example |
|---|---|
| Branch | `DBS-12` |
| Commit message | `DBS-12 add team stats endpoint` |
| Pull request title | `DBS-12 Team stats endpoint` |

- Commit messages start with the task key, followed by a **space** and a short summary.
  Add a body (after an empty line) describing what was changed and why.
- Do not use `_` or other characters right after the key (`DBS-12_fix`):
  Jira may not recognize it.
- Jira links branches, commits and pull requests to the task automatically,
  as long as they contain the task key.
- **One task = one branch = one pull request.**
- Follow-up fixes on a task that is already merged: use a suffix
  (`DBS-12-1`, `DBS-12-2`…) and move the task back to *In progress*.
- New work: create a new Jira task.
- Be careful with the dash: `DBS-12-1` is task 12 (fix 1),
  `DBS-121` is a different task.
- The type of work (feature, bug fix…) is defined in the Jira task.
- The description of the change goes in the pull request template.

## Pull requests

### Opening a pull request
- Each pull request covers **one Jira task** only.
- The title starts with the task key (e.g. `DBS-12 Team stats endpoint`).
- Under **Jira task**, write the task key (e.g. `DBS-12`).
- Fill in every section of the template. If a section does not apply, write `N/A`.
- If the work is not finished yet, open the pull request as a **Draft**.

### Review
- Before merging, **another team member must review and approve** the pull request.
- You cannot approve your own pull request.

## AI assistants

- Rules for AI assistants are in `CLAUDE.md` in each repository.
- Custom commands are in `.claude/commands/` and `.cursor/commands/`.
  Run `/recap` in the AI chat before starting a task to see recent changes and open branches.

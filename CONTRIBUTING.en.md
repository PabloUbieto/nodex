<p align="center">
  <a href="CONTRIBUTING.md">Español</a> | <b>English</b>
</p>

# Contributing guide

Working rules for the repository: branches, commits and Pull Requests. They are enforced by GitHub rulesets and the **PR checks** action.

## Branches

| Branch | Purpose |
|---|---|
| `main` | Final delivery. It is locked and is not touched until delivery. |
| `develop` | Integration. It is the default branch and only changes through Pull Requests. |
| `feature/pablo` | Pablo's working branch. |
| `feature/alvaro` | Álvaro's working branch. |

Each person works only on their own `feature` branch. These branches are never deleted or rewritten: no force push.

## Workflow

1. Update your branch with the latest changes from `develop`.
2. Make small commits on your branch and push them.
3. Open a Pull Request from your branch to `develop` and fill in the template (Summary, Changes and Notes).
4. Assign the PR to yourself and make sure **Check conventions** is green.
5. The repository owner merges using **Create a merge commit**.
6. When the work is finished, open a single PR from `develop` to `main`.

## Commits and PR titles

[Conventional Commits](https://www.conventionalcommits.org/) are used, written in English: `type(scope): description in imperative mood`. The scope is optional.

| Type | Use |
|---|---|
| `feat` | New feature or page |
| `fix` | Bug fix |
| `docs` | Documentation |
| `style` | Formatting, no logic change |
| `refactor` | Restructuring without changing behavior |
| `test` | Tests |
| `chore` | Configuration and maintenance |
| `ci` | Automation (GitHub Actions) |

Examples: `feat(homepage): add hero banner`, `docs(readme): update branding paths`.

One purpose per commit and per PR.

## Automated checks

The **PR checks** action reviews every Pull Request to `develop` or `main`:

- Pull Requests to `develop` are only accepted from `feature/pablo` or `feature/alvaro`.
- Pull Requests to `main` are only accepted from `develop`.
- The PR title and all its commits must follow Conventional Commits.

## File style

`.editorconfig` defines encoding, indentation and the final newline. All files end with an empty line.

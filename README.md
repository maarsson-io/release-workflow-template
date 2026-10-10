# Semi-automated Versioning Workflow

Zero-dependency GitHub Actions workflow templates for semi-automated semantic versioning and release tagging, intended for solo developers and small teams.

The workflows automate release PR titles and version tags. They suggest the next patch version while leaving the final version number under the developer's control. Minor and major releases remain a deliberate human decision.

## Templates

| Template | Branching strategy |
| --- | --- |
| [Three-stage](templates/three-stage/README.md) | `develop → staging → master` |
| [Two-stage](templates/two-stage/README.md) | `develop → master` |

The three-stage template includes a release candidate step on `staging`. The two-stage template releases directly from `develop` to `master` without staging.

## Installation

Choose an available template and copy its `.github/workflows/` files into your repository's `.github/workflows/` directory. Follow the template's README for requirements, merge settings, and usage.

The workflow files are stored under `templates/` so each variant can be copied independently.

## Features

- Automatic patch version suggestion
- Manual minor/major version selection
- Automatic release PR title generation
- Automatic version tag creation
- Idempotent tag creation
- Safe failure when release metadata is invalid
- No GitHub Apps or Personal Access Tokens
- No Conventional Commits required
- No changelog generation

## Customization

Each template contains standalone workflow files. Customize branch names, commit title format, release and tag prefixes, or version bump logic in the copied files as needed.

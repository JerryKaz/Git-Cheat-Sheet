<div align="center">

# Git, GitHub & CI/CD Cheat Sheet

**Every Git command you need, in the order you'll use it. Click any command to copy it.**

[**Live demo →**](https://jerrykaz.github.io/Git-Cheat-Sheet/)

![HTML](https://img.shields.io/badge/HTML-single_file-4B5320?style=flat-square)
![Dependencies](https://img.shields.io/badge/dependencies-none-4B5320?style=flat-square)
![Offline](https://img.shields.io/badge/works-offline-4B5320?style=flat-square)
![Deploy](https://img.shields.io/github/actions/workflow/status/JerryKaz/Git-Cheat-Sheet/static.yml?branch=main&label=pages&style=flat-square)

<img src="https://github.com/user-attachments/assets/e3643ef4-901d-4f9f-8632-5372a655bfe0" alt="Screenshot of the Git cheat sheet: army-green hero banner, section navigation and searchable command list" width="900">

</div>

## What's inside

| | |
|---|---|
| **135+ commands** | From `git init` to `git bisect`, each with a one-line explanation and a copy button |
| **4 step-by-step guides** | Put a new project on GitHub, use the GitHub CLI, set up an SSH key, and the daily branch → PR flow |
| **4 diagrams** | Git's four areas, the publish-to-GitHub flow, feature branching, and a CI/CD pipeline |
| **4 GitHub Actions workflows** | CI, a test matrix, GitHub Pages deploy, and a tag-triggered release, ready to copy into `.github/workflows/` |
| **GitHub CLI section** | `gh` commands for repos, pull requests, Actions runs, secrets and releases |

### Sections, in workflow order

`00` How Git works → `01` Put your project on GitHub → `02` Start a repository → `03` Configure → `04` Stage → `05` Commit → `06` Branch → `07` Sync with GitHub → `08` Merge & rebase → `09` Inspect history → `10` Stash → `11` Undo & recover → `12` Tags & releases → `13` Advanced → `14` GitHub CLI → `15` CI/CD with GitHub Actions

## Features

- **One-click copy.** Click a command or its button, and a toast confirms it. Each guide also has a **Copy all** button for the whole script.
- **Instant search.** Filters commands, guide steps and workflow files as you type. Press <kbd>/</kbd> to focus the search box and <kbd>Esc</kbd> to clear it.
- **Safety cues.** Commands that can delete work (`reset --hard`, `clean -fd`, force push) are marked **Destructive**, and `<placeholders>` are highlighted so you remember to replace them.
- **iOS-style interface.** Frosted-glass header, grouped lists, segmented controls and an army-green accent.
- **Light and dark mode.** Follows your system setting, and the toggle remembers your choice.
- **Responsive and printable.** Works at phone width and prints cleanly as a reference sheet.
- **No build step.** A single `index.html` with inline CSS, JavaScript and SVG icons. No frameworks and no CDN calls, so it works offline.

## Usage

**Online:** open the [live demo](https://jerrykaz.github.io/Git-Cheat-Sheet/).

**Locally:** clone the repo and open `index.html` in any browser.

```bash
git clone https://github.com/JerryKaz/Git-Cheat-Sheet.git
cd Git-Cheat-Sheet
open index.html        # macOS  ·  start index.html on Windows  ·  xdg-open on Linux
```

## Deployment

The site deploys to GitHub Pages automatically through [`.github/workflows/static.yml`](.github/workflows/static.yml) on every push to `main`. To deploy your own fork, go to **Settings → Pages** and set **Source** to **GitHub Actions**.

## Customising

All content lives in plain JavaScript arrays near the bottom of `index.html`, so you can add commands without touching the markup.

```js
// A reference section: each item is [command, description, isDestructive?]
{ id: "stash", short: "Stash", icon: "stash", title: "Stash work in progress", items: [
  ["git stash", "Shelve uncommitted changes"],
  ["git stash drop stash@{<n>}", "Delete one stash"],
]},
```

| To change | Edit |
|---|---|
| Reference commands | `SECTIONS` array |
| Step-by-step guides | `GUIDES` array |
| Workflow YAML | `<script type="text/plain" id="yaml-…">` blocks |
| Diagrams | `<template id="tpl-…">` SVG blocks |
| Colours | CSS variables in `:root` (light) and `:root[data-theme="dark"]` |

Text wrapped in `<angle brackets>` is highlighted as a placeholder automatically, and the navigation, step numbers and command count all update themselves.

## Contributing

Spotted a missing command or a mistake? Open an issue or a pull request:

```bash
git switch -c fix/<short-description>
# edit index.html
git commit -am "Add <command> to <section>"
git push -u origin fix/<short-description>
gh pr create --fill
```

## Author

**Jerry**, Software Engineer · [jerrymyron.com](https://jerrymyron.com) · [GitHub](https://github.com/JerryKaz) · [LinkedIn](https://linkedin.com/in/jerrymyron-80a65a37a)

If this saved you a trip to Stack Overflow, consider giving it a ⭐

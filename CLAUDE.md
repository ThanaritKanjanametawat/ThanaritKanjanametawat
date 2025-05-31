# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is ThanaritKanjanametawat's GitHub profile repository. It contains a README.md that is displayed on the GitHub profile page and includes:
- Professional information and tech stack
- GitHub statistics and contribution visualizations
- A contribution snake animation generated via GitHub Actions

## Key Files and Structure

- `README.md` - The main profile README displayed on GitHub
- `.github/workflows/snake.yml` - GitHub Action workflow that generates the contribution snake animation

## GitHub Actions

### Snake Generation Workflow
- **File**: `.github/workflows/snake.yml`
- **Schedule**: Runs every 12 hours and on push to main branch
- **Output**: Generates SVG files in the `output` branch
- **Files created**:
  - `github-contribution-grid-snake.svg` (light mode)
  - `github-contribution-grid-snake-dark.svg` (dark mode)

## Common Tasks

### Updating the Snake Animation
The snake animation is displayed using picture tags that reference the SVGs from the `output` branch:
```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ThanaritKanjanametawat/ThanaritKanjanametawat/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/ThanaritKanjanametawat/ThanaritKanjanametawat/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/ThanaritKanjanametawat/ThanaritKanjanametawat/output/github-contribution-grid-snake.svg">
</picture>
```

### Checking Workflow Status
Use GitHub CLI to check workflow runs:
```bash
gh run list --workflow=snake.yml
```

## Important Notes

- The `output` branch is automatically managed by the GitHub Action
- Changes to README.md are immediately reflected on the GitHub profile after pushing
- The snake animation requires the workflow to run successfully at least once to generate the SVG files
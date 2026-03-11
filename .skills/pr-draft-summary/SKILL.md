# pr-draft-summary

## Purpose
Generate a markdown PR summary grouped by service, based on git diff and commit log.

## Trigger
When work is finished and ready to commit/PR.

## What it does
1. Reads `git diff` and `git log` for the current branch
2. Groups changed files by service directory
3. Outputs a markdown-formatted change summary

## Usage
```bash
bash .skills/pr-draft-summary/scripts/summary.sh
```

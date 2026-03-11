# code-change-verification

## Purpose
Auto-detect which services were changed and run their lint/type-check/build verification.

## Trigger
After any code modification is complete.

## What it does
1. Reads `git diff --name-only` to identify changed service directories
2. Runs the appropriate verification command per service:
   - Python services → `poetry run mypy app && poetry run flake8 app`
   - tgo-web → `yarn type-check && yarn lint && yarn build`
   - tgo-widget-app → `npm run build`
   - tgo-device-agent → `go vet ./...`
3. Outputs pass/fail per service

## Usage
```bash
bash .skills/code-change-verification/scripts/verify.sh
```

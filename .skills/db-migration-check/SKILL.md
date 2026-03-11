# db-migration-check

## Purpose
Verify that model/schema changes have corresponding Alembic migration files.

## Trigger
When `models/` directory files are modified.

## What it does
1. Checks `git diff` for `models/*.py` or `models/**/*.py` changes
2. Checks for new `alembic/versions/*.py` or `migrations/versions/*.py` files
3. Reports error if model changes exist without corresponding migration

## Usage
```bash
bash .skills/db-migration-check/scripts/check.sh
```

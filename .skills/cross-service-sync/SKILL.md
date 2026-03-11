# cross-service-sync

## Purpose
Detect schema/type/API interface changes and identify files in other services that may need sync.

## Trigger
When schemas, types, or API response structures are modified.

## What it does
1. Detects changed schema/type files
2. Extracts field names and type identifiers
3. Searches other services for matching references
4. Outputs files that may need sync updates

## Usage
```bash
bash .skills/cross-service-sync/scripts/check.sh
```

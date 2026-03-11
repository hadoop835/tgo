# streaming-protocol-check

## Purpose
Check streaming protocol changes for consistency across all consuming services.

## Trigger
When streaming, SSE, WuKongIM, or json-render code is modified.

## What it does
1. Detects changes in streaming-related paths
2. Lists all files across services that handle the same protocol
3. Highlights potential inconsistencies

## Usage
```bash
bash .skills/streaming-protocol-check/scripts/check.sh
```

# implementation-strategy

## Purpose
Analyze changed files to identify affected services, dependencies, and required sync points before implementation.

## Trigger
Before modifying runtime, API, or cross-service code.

## What it does
1. Analyzes `git diff` file paths
2. Maps files to service ownership
3. Outputs affected services and their dependency relationships
4. Lists upstream/downstream services that may need sync

## Usage
```bash
bash .skills/implementation-strategy/scripts/analyze.sh [file1 file2 ...]
```

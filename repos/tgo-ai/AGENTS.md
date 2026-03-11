# tgo-ai — AGENTS.md

> Port: 8081 · Entry: `app/main.py` · Prefix: `/api/v1`

## Rules

- Chat link changes must verify both `stream=false` and `stream=true` paths
- Change schema/types first, then service and router
- Model structure changes must include Alembic migration
- Cross-service calls go through `app/services/*` — no hardcoded URLs or private implementation details

## Key Paths

| Area | Files |
|------|-------|
| Chat | `app/api/v1/chat.py` → `app/services/chat_service.py` |
| Orchestration | `app/runtime/supervisor/` |
| Tools | `app/runtime/tools/`, `app/services/tool_executor.py` |
| Streaming | `app/streaming/` |
| Schemas | `app/schemas/` |
| Models | `app/models/` |

## Constraints

- No `Any` in core interfaces
- No bare `dict` for business objects
- SSE chunk format and event order are stable API — do not break
- External addresses from `app/config.py` + `.env` only
- API input/output must be modeled in `app/schemas/*`

## Verify

```bash
poetry run mypy app && poetry run flake8 app && poetry run pytest
```

FROM python:3.11-slim

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /app

COPY uv.lock pyproject.toml README.md ./
RUN uv sync --frozen --no-cache

COPY src/philoagents philoagents/
COPY tools tools/

ENV PYTHONPATH=/app

EXPOSE 8000

CMD ["/app/.venv/bin/uvicorn", "philoagents.infrastructure.api:app", "--host", "0.0.0.0", "--port", "8000"]

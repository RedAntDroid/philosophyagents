FROM python:3.11-slim

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /app

COPY uv.lock pyproject.toml README.md ./
RUN uv sync --frozen --no-cache

COPY src/philoagents philoagents/
COPY tools tools/

ENV PYTHONPATH=/app

# Let your Python file handle the port
CMD ["uv", "run", "python", "-m", "philoagents.infrastructure.api"]
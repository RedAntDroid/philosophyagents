FROM python:3.11-slim

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /app

COPY uv.lock pyproject.toml README.md ./
RUN uv sync --frozen --no-cache

COPY src/philoagents philoagents/
COPY tools tools/

ENV PYTHONPATH=/app

# Let your Python file handle the port
# Tells the uv server to listen on all network interfaces (0.0.0.0) on port 10000
CMD ["uv", "run", "--host", "0.0.0.0", "--port", "10000", "-m", "philoagents.infrastructure.api"]
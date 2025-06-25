FROM python:3.11-slim

# Install uv
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

# Set working directory
WORKDIR /app

# Install dependencies
COPY uv.lock pyproject.toml README.md ./
RUN uv sync --frozen --no-cache

# Copy source code
COPY src/philoagents philoagents/
COPY tools tools/

# Expose port 8000 to let Render detect it
EXPOSE 8000

# Start FastAPI with uvicorn
CMD ["uvicorn", "philoagents.infrastructure.api:app", "--host", "0.0.0.0", "--port", "8000"]

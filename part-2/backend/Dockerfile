FROM python:3.12-slim

RUN pip install uv

WORKDIR /app

COPY pyproject.toml uv.lock ./

RUN uv sync --frozen --no-dev

COPY main.py ./

EXPOSE 8000

CMD ["uv", "run", "fastapi", "run", "main.py", "--port", "8000"]
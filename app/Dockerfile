FROM python:3.11-slim

WORKDIR /app

# Create non-root user (security best practice)
RUN useradd -m appuser

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app/ app/

USER appuser

EXPOSE 5000

CMD ["python", "app/main.py"]

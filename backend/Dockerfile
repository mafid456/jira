FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy backend files
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app/ ./app

# Expose port
EXPOSE 8000

# Run Uvicorn
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

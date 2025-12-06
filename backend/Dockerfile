# Use Python 3.12 slim
FROM python:3.12-slim

# Create app directory
WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy all backend code
COPY . .

# Expose port 5000
EXPOSE 5000

# Start the Flask app
CMD ["python", "app.py"]

# Use the official slim Python image
FROM python:3.11-slim

# Set the working directory
WORKDIR /app

# Copy dependency file first for efficient caching
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Expose Flask's default port
EXPOSE 5000

# Run the Flask app
CMD ["python", "app.py"]

# Use a minimal Python image based on Alpine Linux
FROM python:3.9-alpine

# Set working directory
WORKDIR /app

# Copy dependency file
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Python script
COPY script.py .

# Run the script
CMD ["python", "script.py"]

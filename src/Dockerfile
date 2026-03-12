# Use a lightweight Python base image
FROM python:3.9-slim-buster

# Set working directory inside the container
WORKDIR /app

# Copy requirements first (adjust path if needed)
COPY ./requirements.txt ./ 

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY ./run.py ./ 
COPY ./app/ ./app

# Expose the port used by Flask
EXPOSE 5000

# Run the application
CMD ["python", "run.py"]

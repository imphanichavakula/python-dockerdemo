# Use a lightweight Python base image
FROM python:3.9-slim-buster

# Set working directory inside the container
WORKDIR /app

# Step 1: copy only requirements for caching
COPY src/requirements.txt ./

# Step 2: install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 3: copy the rest of the source code
COPY src/run.py .
COPY src/app/ ./app

# Expose the port used by Flask
EXPOSE 5000

# Run the application
CMD ["python", "run.py"]

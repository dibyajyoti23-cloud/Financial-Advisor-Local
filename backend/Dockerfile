# backend/Dockerfile

# Use an official lightweight Python image
FROM python:3.11-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the backend application code
COPY . .

# Expose the port the app runs on
EXPOSE 5000

# Command to run the application using a production server
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "app:app"]
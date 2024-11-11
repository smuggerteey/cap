# Use the official Python image
FROM python:3.8-slim

# Set the working directory inside the container
WORKDIR /app

# Copy requirements.txt for dependency installation
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Set environment variable to tell Flask it's in production mode
ENV FLASK_ENV=production

# Set the default command to run when the container starts
CMD ["flask", "run", "--host=0.0.0.0"]

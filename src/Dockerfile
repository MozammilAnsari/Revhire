# Use the official Python image as a base image
FROM python:3.9-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /app

# Copy the contents of the src directory to the working directory
COPY . .

# Install any dependencies
RUN pip install -r requirements.txt

# Expose port 80 to the outside world
EXPOSE 80

# Command to run the FastAPI application
CMD ["python", "create_tables.py"]

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
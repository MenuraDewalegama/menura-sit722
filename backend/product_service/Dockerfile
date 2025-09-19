# Use a lightweight official Python image as the base.
FROM python:3.13-slim

# Set the working directory inside the container.
WORKDIR /app

# Copy the requirements file into the container.
COPY requirements.txt .

# Install the dependencies from the requirements.txt file.
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

# Copy the entire application code into the container.
COPY . .

# Expose the port that the FastAPI application will run on.
EXPOSE 8000

# Define the command to run the application when the container starts.
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
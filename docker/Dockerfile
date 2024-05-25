# Use an official Python runtime as a parent image
FROM python:3.9-slim-buster

# Set the working directory in the container
WORKDIR /app

# Copy requirements file to the container
COPY requirements.txt ./ 

# Install packages with user permissions and update PYTHONPATH
RUN pip install --user -r requirements.txt \
    && ENV PYTHONPATH="${PYTHONPATH}:/root/.local/lib/python3.9/site-packages"

# Copy the application code
COPY . .

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]


# Use Python 3.12 Slim as base image
FROM python:3.12-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . .

# Install system dependencies required for mysqlclient
RUN apt-get update && apt-get install -y \
    pkg-config \
    default-libmysqlclient-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Install required Python dependencies, including mysqlclient
RUN pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt && \
    pip install python-dotenv

ENV MYSQL_HOST=sql_cont
ENV MYSQL_USER=external_user
ENV MYSQL_PASSWORD=password
ENV MYSQL_DB=my_database
# Expose port 5000 (Flask default port)
EXPOSE 5000

# Define the default command to run the Flask app
CMD ["python", "app.py"]

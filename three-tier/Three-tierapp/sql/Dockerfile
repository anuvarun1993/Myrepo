# Use the official MySQL image as a base
FROM mysql:8.0

# Set environment variables for the MySQL database and user
ENV MYSQL_USER=external_user
ENV MYSQL_PASSWORD=password
ENV MYSQL_DATABASE=test
ENV MYSQL_ROOT_PASSWORD=root

# Expose port 3306 to allow connections to the database
EXPOSE 3306

# Start the MySQL server when the container is run
CMD ["mysqld"]

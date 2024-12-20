# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update the package list and upgrade all installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED file to prevent installation errors
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the api.py file to the working directory
COPY ./api.py /app/api.py

# Set the command to run the Flask application
CMD ["python3", "api.py"]

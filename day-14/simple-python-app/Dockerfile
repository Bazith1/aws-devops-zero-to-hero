# Base image
FROM python:3.8

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file
COPY requirements.txt .

# Install the project dependencies
RUN pip install -r requirements.txt

# Copy the application code into the container
COPY . .
#COPY: This is a Dockerfile command that copies files and directories from the source on the host system into the destination inside the Docker image.

. (first dot): The first dot represents the source directory on the host system, which is the current directory where the Dockerfile is located (often referred to as the build context). It means "copy everything in the current directory."

. (second dot): The second dot represents the destination directory inside the Docker image. It is usually set to the current working directory in the container (often specified earlier in the Dockerfile using the WORKDIR instruction). If not specified, it defaults to the root directory (/) inside the image.
# Expose the port the Flask application will be listening on
EXPOSE 5000

# Set environment variables, if necessary
# ENV MY_ENV_VAR=value

# Run the Flask application
CMD ["python", "app.py"]

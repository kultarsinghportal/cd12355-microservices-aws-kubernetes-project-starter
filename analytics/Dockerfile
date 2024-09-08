
# Use Python Python 3.10 as the base image
FROM public.ecr.aws/docker/library/python:3.10-slim-buster

# Set the working directory inside the container
WORKDIR /app

# Copy the current directory contents to the container at /app
COPY /analytics/ /app

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r /analytics/requirements.txt

# Expose port 5000
EXPOSE 5153

# Set an environment variable
ENV DB_USERNAME=postgres
ENV DB_PASSWORD=newpassword
ENV DB_HOST=host.docker.internal
ENV DB_PORT=5432
ENV DB_NAME=postgres

# Run the application when the container starts
CMD ["python", "app/app.py"]


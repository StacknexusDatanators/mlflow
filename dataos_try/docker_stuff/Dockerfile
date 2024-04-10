# Dockerfile for hosting an MLflow server

# Use the official Python image as the base image
FROM python:3.8-slim

# Set environment variables
ENV MLFLOW_HOME=/mlflow
ENV MLFLOW_SERVER_HOST=0.0.0.0
ENV MLFLOW_SERVER_PORT=5000

# Install MLflow
RUN pip install mlflow

# Create a directory for MLflow artifacts
RUN mkdir -p $MLFLOW_HOME

# Set the working directory
WORKDIR $MLFLOW_HOME

# Expose the MLflow server port
EXPOSE $MLFLOW_SERVER_PORT

# Start the MLflow server
CMD ["mlflow", "server", "--host", "0.0.0.0", "--port", "5000"]
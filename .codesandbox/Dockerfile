# Pull base image
FROM python:3.10-slim-buster

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
# Expose port 8000
EXPOSE 8000

# Use gunicorn on port 8000
CMD ["gunicorn", "--bind", ":8000", "--workers", "2", "django_project.wsgi"]
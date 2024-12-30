# Use official Python image
FROM python:3.9

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
WORKDIR /usr/src/app

# Install dependencies
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# Copy project files
COPY . .

# Expose port and run server
EXPOSE 8000
CMD ["gunicorn", "--bind", ":8000", "backend.wsgi:application"]

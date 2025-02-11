FROM python:3.11

# Set the working directory inside the container
WORKDIR /data

# Install Django globally as needed
RUN pip install django==3.2

# Copy all files from the current directory to the container's /data directory
COPY . .

# Create a virtual environment in /opt/venv
RUN python3 -m venv /opt/venv

# Upgrade pip and install required packages within the virtual environment
RUN /opt/venv/bin/pip install --upgrade pip setuptools
RUN /opt/venv/bin/pip install -r requirements.txt

# Run Django migrations using the virtual environment Python
RUN /opt/venv/bin/python manage.py migrate

# Expose port 8000 for the Django app
EXPOSE 8000

# Use the virtual environment's Python binary to run the Django development server
CMD ["/opt/venv/bin/python", "manage.py", "runserver", "0.0.0.0:8000"]

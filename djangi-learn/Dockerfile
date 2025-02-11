FROM python:3

WORKDIR /data

RUN pip install django==3.2

COPY . .

RUN python3 -m venv /opt/venv
RUN /opt/venv/bin/pip install --upgrade pip setuptools
RUN /opt/venv/bin/pip install -r requirements.txt

RUN /opt/venv/bin/python manage.py migrate

EXPOSE 8000

CMD ["python","manage.py","runserver","0.0.0.0:8000"]



FROM python:3.8  

ENV PYTHONDONTWRITEBYTECODE 1

ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY . /app/

RUN apt-get upgrade 

RUN pip install --upgrade pip


RUN pip install -r requirements.txt

RUN python -m pip install psycopg2

RUN python manage.py makemigrations

RUN python manage.py migrate

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8001" ]

FROM python:3.9.2

COPY . /usr/src/app
WORKDIR /usr/src/app

RUN pip install --no-cache-dir -r requirements.txt

RUN python manage.py makemigrations
RUN python manage.py migrate

RUN chmod 777 /usr/src/app

ENTRYPOINT [ "docker-entrypoint.sh" ]
EXPOSE 8000
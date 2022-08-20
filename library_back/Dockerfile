FROM python:3.10

WORKDIR /library_back

COPY . /library_back/

RUN pip install -r requirements.txt

RUN python manage.py makemigrations

RUN python manage.py migrate

RUN python manage.py runserver

COPY . .
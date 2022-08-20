FROM python:3.10

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

RUN mkdir /library_back

WORKDIR /library_back

COPY requirements.txt /library_back/

RUN pip install -r requirements.txt

COPY . .
# Das ist das Dockerfile um ein Build aus dem Quellcode zu bauen
FROM python:latest as initial

COPY . /mppsolar/
RUN apt-get update ; \
    apt-get install -y pkg-config libsystemd-dev gcc libpq-dev; \
    pip install --upgrade pip ; \
    pip install paho-mqtt systemd-python pymongo psycopg2; \
    #pip install mppsolar ; \
    pip install -e /mppsolar/ 

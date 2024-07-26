FROM python:3.8.10-slim

COPY . /app
WORKDIR /app

RUN apt update -y && \
    apt install -y build-essential libpq-dev && \
    pip install --upgrade pip setuptools wheel && \
    pip install -r requirements.txt

ENV DB_USERNAME myuser
ENV DB_PASSWORD mypassword
ENV DB_HOST 127.0.0.1
ENV DB_PORT 5433
ENV DB_NAME mydatabase

CMD [ "python",  "app.py" ]

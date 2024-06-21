FROM python:3.8.10-slim

COPY . /app
WORKDIR /app

RUN apt update -y && \
    apt install -y build-essential libpq-dev && \
    pip install --upgrade pip setuptools wheel && \
    pip install -r requirements.txt

CMD [ "python",  "app.py" ]

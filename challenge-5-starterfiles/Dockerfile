FROM python:3

RUN apt-get clean \
    && apt-get -y update

RUN apt-get -y install \
    python3

WORKDIR /app

COPY requirements.txt /app/requirements.txt
RUN pip install -r requirements.txt

COPY app.py /app/app.py
COPY templates /app/templates

EXPOSE 8000

CMD [ "python3", "app.py" ]
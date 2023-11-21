FROM python:3.9

ENV PORT 80
ENV HOST 0.0.0.0

EXPOSE 80

RUN apt-get update -y && \
    apt-get install -y python3-pip

COPY ./requirements.txt /app/requirements.txt
COPY ./templates /app/templates
COPY ./templates /app
COPY ./Forecasting /app/Forecasting
COPY ./Flask /app/Flask
COPY ./React /app/React


WORKDIR /app

RUN pip install --upgrade pip

RUN pip install -r requirements.txt

COPY . /app


ENTRYPOINT ["python", "app.py"]

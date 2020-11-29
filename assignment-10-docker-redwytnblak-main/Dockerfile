FROM ghcr.io/ustseis615/ubuntu:xenial

LABEL maintainer="Hytham Aly, aly03229@stthomas.edu"

EXPOSE 8080

RUN apt-get update
RUN apt-get install python-pip -y
RUN apt-get install python-dev -y

COPY /app/site.py /app/
COPY /app/requirements.txt /app/

WORKDIR /app
RUN pip install -r requirements.txt

CMD [ "/app/site.py" ]
ENTRYPOINT ["python"]

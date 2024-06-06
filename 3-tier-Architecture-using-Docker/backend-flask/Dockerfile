FROM ubuntu:22.04
RUN apt-get update && apt-get install -y python
RUN apt-get install -y python3-pip mysql-server libmysqlclient-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip3 install -r requirements.txt
ADD . /code/

CMD ["python3", "backend.py" ]


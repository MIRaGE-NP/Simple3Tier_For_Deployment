FROM ubuntu:22.04
RUN apt-get update && apt-get install -y python3
RUN apt-get install -y python3-pip mysql-server libmysqlclient-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip3 install -r requirements.txt
RUN pip3 install -r requirements.txt && \
    pip3 install jinja2 && \
    pip3 install --upgrade flask jinja2 && \
    pip3 install install urllib3 six && \
    pip install --upgrade requests urllib3 six
ADD . /code/
CMD ["python3", "backend.py" ]


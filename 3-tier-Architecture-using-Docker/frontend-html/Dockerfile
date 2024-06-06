FROM python:3
RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip3 install -r requirements.txt && \
    pip3 install jinja2 && \
    pip3 install --upgrade flask jinja2 && \
    pip3 install install urllib3 six && \
    pip install --upgrade requests urllib3 six
ADD . /code/
EXPOSE 5001
CMD ["python3", "front.py" ]

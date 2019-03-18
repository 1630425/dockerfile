FROM chengt/python:3.6.8-alpine3.8

RUN pip install wxpy
RUN pip install requests

COPY *.py /
CMD ["python3 main.py”]
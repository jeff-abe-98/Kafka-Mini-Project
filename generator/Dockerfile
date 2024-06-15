# Dockerfile
FROM python:3.11

WORKDIR /usr/app

ADD ./requirements.txt ./
RUN pip install -r requirements.txt
ADD ./ ./

CMD ["python", "app.py"]
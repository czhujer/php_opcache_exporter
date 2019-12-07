FROM python:2-alpine
LABEL maintainer="Narate Ketram <koonnarate@gmail.com>"
WORKDIR /app
ADD ./docker/python/requirements.txt .
RUN pip install -r requirements.txt
ADD ./php_opcache_exporter.py .
EXPOSE 9462
CMD ["python", "php_opcache_exporter.py"]

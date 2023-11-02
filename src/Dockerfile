FROM alpine:latest

RUN apk add --update-cache python3 python3-dev py3-pip build-base && rm -rf /var/cache/apk/*

COPY requirements.txt /usr/src/app/

RUN pip3 install --no-cache-dir -r /usr/src/app/requirements.txt

COPY app.py /usr/src/app/

EXPOSE 5000

CMD ["python3", "/usr/src/app/app.py"]

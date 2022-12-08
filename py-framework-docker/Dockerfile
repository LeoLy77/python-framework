FROM python:3.10-slim

WORKDIR /app/

COPY requirements.txt .
RUN apk add --no-cache py3-pip && \
    pip3 install -r requirements.txt && \
    apk del py3-pip
# RUN pip install -r requirements.txt
COPY py.py .

ENTRYPOINT ["python", "py.py"]
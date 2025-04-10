#Stage 1

FROM python:3.7 AS builder

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt


#Stage 2
FROM python:3.7-slim

WORKDIR /app

COPY --from=builder /usr/local/lib/python3.7/site-packages/  /usr/local/lib/python3.7/site-packages/

#COPY --from=builder /usr/local/bin/ /usr/local/bin/

#COPY requirements.txt .
#RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENTRYPOINT ["python","run.py"]

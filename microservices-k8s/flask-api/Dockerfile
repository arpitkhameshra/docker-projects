FROM python:3.9-alpine

WORKDIR /app

COPY . .

RUN pip install flask

RUN pip install -r requirements.txt

EXPOSE 5000

ENV FLASK_APP=app.py

ENV FLASK_RUN_HOST=0.0.0.0

CMD ["python","app.py"]

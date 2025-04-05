FROM python:3.9 AS big-stage

WORKDIR /app/backend

COPY requirements.txt /app/backend
RUN pip install -r requirements.txt


FROM python:3.9-slim-bullseye

COPY --from=big-stage /usr/local/lib/python3.9/site-packages/ /usr/local/lib/python3.9/site-packages/

COPY . /app/backend

EXPOSE 8000

CMD python /app/backend/manage.py runserver 0.0.0.0:8000

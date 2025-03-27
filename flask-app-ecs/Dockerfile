#Stage 1

FROM python:3.7 AS big-stage

WORKDIR /app

COPY . .

#Stage 2
FROM python:3.9-slim-bullseye

COPY --from=big-stage /app /app


ENTRYPOINT ["python","app.py"]

FROM python:3.9 AS builder

WORKDIR /api

COPY ./requirements.txt /api/requirements.txt

RUN --mount=type=cache,target=/root/.cache/pip pip install -r requirements.txt

COPY ./src /api

CMD [ "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80", "--reload" ]
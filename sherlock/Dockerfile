FROM python:alpine as build
WORKDIR /wheels
RUN apk update --no-cache \
  && apk add --no-cache \
    g++ \
    gcc \
    libxml2 \
    libxml2-dev \
    libxslt-dev \
    linux-headers
COPY ./sherlock/requirements.txt /opt/sherlock/
RUN pip3 wheel -r /opt/sherlock/requirements.txt


FROM python:alpine
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"
WORKDIR /opt/sherlock
COPY --from=build /wheels /wheels
COPY ./sherlock/* /opt/sherlock/
RUN pip3 install -r requirements.txt -f /wheels \
  && rm -rf /wheels \
  && rm -rf /root/.cache/pip/*

ENTRYPOINT ["python", "sherlock.py"]

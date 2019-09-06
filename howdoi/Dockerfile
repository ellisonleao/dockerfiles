FROM python:alpine
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apk --no-cache add \
    gcc \
    musl-dev \
    libxml2-dev \
    libxslt-dev \
	&& pip3 --no-cache-dir install howdoi

ENTRYPOINT [ "howdoi" ]

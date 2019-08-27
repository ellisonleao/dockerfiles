FROM alpine:latest
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apk --no-cache add \
	ca-certificates \
	python3 \
    python3-dev \
    gcc \
    libxml2-dev \
    musl-dev \
    libxslt-dev \
	&& pip3 --no-cache-dir install howdoi

ENTRYPOINT [ "howdoi" ]

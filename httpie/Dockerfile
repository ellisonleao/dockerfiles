FROM alpine:latest
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apk --no-cache add \
	ca-certificates \
	python3 \
	&& pip3 install --no-cache-dir httpie httpie-unixsocket

ENTRYPOINT [ "http" ]

FROM alpine:latest
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apk --no-cache add \
	ca-certificates \
	python3 \
	&& pip3 --no-cache-dir install speedtest-cli

ENTRYPOINT [ "speedtest-cli" ]

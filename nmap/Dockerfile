FROM debian:bullseye-slim
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apt-get update && apt-get install -y \
	nmap \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "nmap" ]

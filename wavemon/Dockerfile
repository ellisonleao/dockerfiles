FROM debian:bullseye-slim
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN apt-get update && apt-get install -y \
	wavemon \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "wavemon" ]

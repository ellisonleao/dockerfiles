# Build Container
FROM golang:alpine AS build
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN	apk --no-cache add \
	gcc \
	git \
	libc-dev

ENV PATH /go/bin:/usr/local/go/bin:$PATH
ENV GOPATH /go

RUN go get -u -v github.com/projectdiscovery/subfinder/cmd/subfinder

FROM alpine

COPY --from=build /go/bin/subfinder /usr/bin/subfinder

ENTRYPOINT ["subfinder"]

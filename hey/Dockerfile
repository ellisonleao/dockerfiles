FROM golang:alpine AS builder
LABEL maintainer "Ellison Leão <ellisonleao@gmail.com>"

RUN	apk --no-cache add \
	gcc \
	git \
	libc-dev

ENV PATH /go/bin:/usr/local/go/bin:$PATH
ENV GOPATH /go

RUN go get github.com/rakyll/hey 

FROM alpine:latest 

COPY --from=builder /go/bin/hey /usr/bin/hey

ENTRYPOINT [ "hey" ]

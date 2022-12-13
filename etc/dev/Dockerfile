FROM golang:1.19.4-bullseye

ARG UID

ENV GOPATH=/go PATH=/home/dev/go/bin:$PATH

RUN go install github.com/cosmtrek/air@latest \
    && go install github.com/go-delve/delve/cmd/dlv@latest \
    && useradd -m -u${UID:-1000} dev \
    && mkdir -p /home/dev/go \
    && chown -R dev:dev /home/dev

USER dev

ENV GOPATH=/home/dev/go:/go

WORKDIR /home/dev/app
CMD air

VOLUME ["/home/dev/app", "/home/dev"]

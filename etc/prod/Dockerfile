FROM golang:1.21.0-bullseye as builder

ENV CGO_ENABLED=0

WORKDIR /app

COPY go.mod .
COPY go.sum .
RUN go mod download

COPY . .
RUN go build -o /tmp/goapi .

FROM scratch
COPY --from=builder /tmp/goapi /
ENTRYPOINT [ "/goapi" ]

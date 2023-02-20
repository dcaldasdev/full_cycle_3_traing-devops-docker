FROM golang AS builder

WORKDIR /app
ADD . /app
RUN go build -o hello hello.go

FROM alpine
WORKDIR /app
COPY --from=builder /app/hello /app
ENTRYPOINT ./hello
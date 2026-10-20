FROM golang:1.25 AS builder
WORKDIR /app
COPY main.go .
RUN go build -o app main.go
FROM scratch
WORKDIR /root/
COPY --from=builder /app/app .
CMD ["./app"]

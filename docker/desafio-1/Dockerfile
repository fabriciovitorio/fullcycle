FROM golang:alpine AS builder

WORKDIR /go/src/desafio-1

COPY . .
RUN go build -o /desafio-1 main.go

FROM scratch

COPY --from=builder /desafio-1 /desafio-1
CMD ["/desafio-1"]
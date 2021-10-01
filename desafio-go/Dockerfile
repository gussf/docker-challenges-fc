FROM golang:1.17 as builder

WORKDIR /go/src/desafio-go

COPY ./ ./

RUN GOOS=linux go build -ldflags="-w -s" -o main .



FROM scratch

COPY --from=builder /go/src/desafio-go/main ./

ENTRYPOINT [ "./main" ]
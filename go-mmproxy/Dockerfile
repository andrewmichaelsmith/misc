FROM golang:alpine AS builder

RUN apk update && apk add --no-cache git
ENV CGO_ENABLED=0
RUN go get github.com/path-network/go-mmproxy

FROM scratch
COPY --from=builder /go/bin/go-mmproxy /go/bin/go-mmproxy
ENTRYPOINT ["/go/bin/go-mmproxy"]


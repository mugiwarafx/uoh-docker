FROM golang:1.18

EXPOSE 8000

ENV PORT=8000
ENV REQUEST_ORIGIN=http://localhost:5000

WORKDIR /usr/src/app

# pre-copy/cache go.mod for pre-downloading dependencies and only redownloading them in subsequent builds if they change
COPY go.mod go.sum ./
RUN go mod download && go mod verify

COPY . .

#RUN go build -v -o /usr/local/bin/app ./...
RUN go build -v -o /usr/src/app ./...
RUN go test ./...

CMD ["./server"]
FROM golang:1.23-bookworm 

WORKDIR /app 

COPY go.mod go.sum ./ 
RUN go mod download

COPY . . 
RUN go build -o build/fizzbuzz 

CMD ["./build/fizzbuzz", "serve", "--port", "8080"]
# Go Protobuf

This repository contains the protocol buffer files for gRPC microservices built with Go. It is designed to be used alongside the [go-middleware](https://github.com/ebenwy5/go-middleware) repository, which provides middleware utilities such as gRPC and RESTful API gateway setup using Echo, and gRPC interceptors for logging.

## Requirements

- Go 1.16 or later
- Protocol Buffers (protoc) v3.18.0 or later
- Go gRPC plugin for protoc

## Usage

This repository should be used together with the [go-middleware](https://github.com/ebenwy5/go-middleware) library, which contains the middleware utilities required for setting up gRPC servers and RESTful APIs. The [go-user](https://github.com/ebenwy5/go-user) and [go-product](https://github.com/ebenwy5/go-product) repositories serve as example projects that demonstrate how to use this protobuf repository together with the go-middleware library.

## Structure

The protocol buffer files are organized in separate directories for each microservice:

- `user/`: Contains the protocol buffer files for the user microservice
- `product/`: Contains the protocol buffer files for the product microservice

## License

[MIT](LICENSE)
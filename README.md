# Go Protobuf

This repository contains the protocol buffer files for gRPC microservices built with Go. It is designed to be used alongside the [go-middleware](https://github.com/ebenwy5/go-middleware) repository, which provides middleware utilities such as gRPC and RESTful API gateway setup using Echo, and gRPC interceptors for logging.

## Requirements

- Go 1.16 or later
- Protocol Buffers (protoc) v3.21.12 or later
- Go gRPC plugin for protoc, which consist of:
  - protoc-gen-go v1.30.0 or later
  - protoc-gen-go-grpc 1.3.0 or later

## Usage

This repository should be used together with the [go-middleware](https://github.com/ebenwy5/go-middleware) library, which contains the middleware utilities required for setting up gRPC servers and RESTful APIs. The [go-user](https://github.com/ebenwy5/go-user) and [go-product](https://github.com/ebenwy5/go-product) repositories serve as example projects that demonstrate how to use this protobuf repository together with the go-middleware library.

## File Generation Syntax

For go files, here the syntax for generating the go files:

`protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative $SRC_DIR/$PROTO_FILENAME.proto`

Where `$SRC_DIR` is your repository name and `$PROTO_FILENAME` is your target proto file to be generated. For example:

`protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative go-product/go-product.proto`
`protoc --proto_path=. --proto_path=PATH/TO/googleapis --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative --grpc-gateway_out=. --grpc-gateway_opt=paths=source_relative --grpc-gateway_opt=logtostderr=true go-user/go-user.proto`

## Structure

The protocol buffer files are organized in separate directories for each microservice:
- `go-user/`: Contains the protocol buffer files for the user microservice
- `go-product/`: Contains the protocol buffer files for the product microservice
- `your-repository-name/`: Put any desired repository name in this manner, and the proto files inside

## TODO
- 

## License

[MIT](LICENSE)
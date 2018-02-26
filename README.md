protoc-gen-grpc
=========================
Protocol Buffers Compiler (protoc) plugin for generating grpc interfaces in TypeScript.

## Aim

This project was forked from [agreatfool/grpc_tools_node_protoc_ts](https://github.com/agreatfool/grpc_tools_node_protoc_ts), and was intended to fix an error in Window10: `%1 XXX not a valid win32 application`

* difference
  * No other tools (or npm global package) need to be installed. such as `protoc`, `grpc_tools`
  * Remove handlebar template engine. 
  * Support: Linux, OSX, Windows

## Install

```bash
npm install protoc-gen-grpc -g
```

## How to use

```bash
# generate js codes
protoc-gen-grpc \
--js_out=import_style=commonjs,binary:./examples/src \
--grpc_out=./examples/src \
--proto_path ./examples/proto \
./examples/proto/book.proto

# generate d.ts codes
protoc-gen-grpc-ts \
--ts_out=service=true:./examples/src \
--proto_path ./examples/proto \
./examples/proto/book.proto
```
## Example

[link to examples](https://github.com/niklaus0823/protoc-gen-grpc/tree/master/examples)
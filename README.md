# netcore-grpc-docker-demo
Playing with netcore + gRPC + docker

### Build Server
```bash
cd ./GrpcGreeter
docker build . -t dz/grpc_greeter:1
```
### Start Server
```bash
docker run -p 5000:5000 --name grpc_greeter dz/grpc_greeter:1
```
### Build Client
```bash
cd ./GrpcGreeterClient
docker build . -t dz/grpc_greeter_client:1
```
### Run Client
```bash
docker run --link grpc_greeter dz/grpc_greeter_client:1
```

## How to run the project
### Create `venv` environment and install dependencies from `requirments.txt`
### Generate protobuf python implementation
```bash
python3 -m grpc_tools.protoc --proto_path=. --python_out=. --grpc_python_out=. data_transfer_api.proto 
```



## How to run docker container of project
### Build docker image
``` docker build -t <image_name> . ```
## Run docker image:
```docker run --net=host <image_name> <server_address> <vervbose> <duration>```

if verbose is 1, then driver expected to print data, that it got from sensors.
Duration is responsible how often driver would send data to the server.Duration measured in seconds.

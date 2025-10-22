# test_containerizing_SAMSRC

## Building
podman build ./ -t samsrcv5 <br>
podman build --build-arg BUILD_VERSION=2.0.0 -t samsrcv5 . <br>

## Running
podman run -it samsrcv5 <br>


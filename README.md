# test_containerizing_SAMSRC

## Building SAMSRC
podman build ./ -t samsrcv5 <br>
podman build --build-arg BUILD_VERSION=2.0.0 -t samsrcv5 . <br>

## Running
podman run -it samsrcv5 <br>


## Create Afni Dockerfile
docker run --rm repronim/neurodocker:latest  generate docker     --pkg-manager yum     --base-image fedora:40     --afni method=binaries version=latest install_r_pkgs=true > afni-binaries-r.Dockerfile

#docker run --rm repronim/neurodocker:latest generate docker --pkg-manager apt --base-image debian:bullseye-slim --afni method=binaries version=latest install_r_pkgs=true > afni-binaries-r.Dockerfile

## Build from afni Dockerfile
podman build -f afni-binaries-r.Dockerfile -t afni



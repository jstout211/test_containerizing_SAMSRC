## To build the container
```
# Build the afni fedora 43 package
podman build -f ./afni-binaries-r.Dockerfile -t afni_fedora
# Build the sam_fedora image from the afni image
podman build -f ./Containerfile -t sam_fedora
```


## To run the container interactively: sam_cov, sam_wts, sam_4d etc are available in the container.  You can mount data locations in the container for processing
`podman run -it sam_fedora`

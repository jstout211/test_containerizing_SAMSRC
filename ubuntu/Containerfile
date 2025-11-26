FROM ubuntu:latest
RUN apt update && apt install -y build-essential libgsl-dev libfftw3-dev git
RUN git clone https://github.com/nih-megcore/SAMsrcV5.git /opt/SAMsrcV5
WORKDIR /opt/SAMsrcV5
RUN make
ENV PATH=${PATH}:/opt/SAMsrcV5/bin
#WORKDIR /opt/SAMsrcV5/bin
#RUN make symlinks
#CMD ["/usr/local/bin/triangle"]

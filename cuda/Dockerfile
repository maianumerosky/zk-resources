FROM nvidia/cuda:11.0.3-devel-ubuntu20.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y update
RUN apt-get install -y build-essential \
                pkg-config \
                libcurl4-openssl-dev \
                libssl-dev \
                ocl-icd-opencl-dev \
                linux-tools-generic \
                linux-tools-$(uname -r) \
                curl

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
ENV PATH="root/.cargo/bin:${PATH}"

FROM ubuntu:22.04

RUN apt update && \
	apt install -y build-essential cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib \
	 git python3 && \
         apt autoremove -y

RUN git clone --recurse-submodules https://github.com/raspberrypi/pico-sdk /pico-sdk
ENV PICO_SDK_PATH=/pico-sdk

WORKDIR /build

ENTRYPOINT ["/bin/bash", "-c", "cmake \"/project\" && make"]

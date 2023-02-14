# PiPico Dockerfile

## Description

This Dockerfile is for those of us who don't want to set the Pico-SDK everytime

Or if it's too complicated or time consuming on their distro

## Build

Just straight forward

`docker build -t thelondev/pipico ./docker`

## Usage

You need to mount the code (root directory with CMakeLists.txt) to /project

And the output directory to /build (where the output will be)

For example:

We have a project in "/projects/traffic-light" and we want to output the .utf2 to "/production/traffic-light"

`docker run -v /projects/traffic-light:/project -v /production/traffic-light:/build thelonedev/pipico`

Replace `thelonedev/pipico` if you built it with a different name

The sdk is installed at /pico-sdk

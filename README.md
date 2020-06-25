# mocha-build
Non-proprietary build environment resources for Mocha

To build the Linux Docker image:

    docker build -t bfxmocha/mocha-build-linux linux

Run bash in a container from the image:

    docker run -ti --rm -v $PWD:/opt/app-root/src:z bfxmocha/mocha-build-linux bash

For further instructions see the upstream docs at [centos/devtoolset-7-toolchain-centos7](https://hub.docker.com/r/centos/devtoolset-7-toolchain-centos7/).

Push the new image to Docker Hub (requires login and permission to
commit to the org):

    docker push bfxmocha/mocha-build-linux


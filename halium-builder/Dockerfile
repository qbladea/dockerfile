FROM debian:latest

RUN apt update -y && apt upgrade -y && dpkg --add-architecture i386 && apt update -y && apt install git gnupg flex bison gperf build-essential zip bzr curl libc6-dev libncurses5-dev:i386 x11proto-core-dev libx11-dev:i386 libreadline6-dev:i386 libgl1-mesa-glx:i386 libgl1-mesa-dev g++-multilib mingw-w64-i686-dev tofrodos python-markdown libxml2-utils xsltproc zlib1g-dev:i386 schedtool liblz4-tool bc lzop imagemagick libncurses5 rsync -y 


CMD groupadd -g ${GID} halium-builder && useradd -g halium-builder -u ${UID} halium-builder && su - halium-builder

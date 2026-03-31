FROM        eclipse-temurin:23-ubi10-minimal

LABEL       author="Softwarenoob" maintainer="admin@softwarenoob.com"
LABEL       org.opencontainers.image.source="https://github.com/DonPedroTV/pterodactyl-images"
LABEL       org.opencontainers.image.licenses="MIT"

RUN         microdnf update -y \
            && microdnf install -y curl ca-certificates openssl git tar gzip sqlite fontconfig tzdata iproute gcc gcc-c++ freetype libstdc++ lsof glibc-locale-source glibc-langpack-en \
            && microdnf clean all \
            && useradd -m -d /home/container container \
            && localedef -i en_US -f UTF-8 en_US.UTF-8

ENV         LC_ALL=en_US.UTF-8
ENV         LANG=en_US.UTF-8
ENV         LANGUAGE=en_US.UTF-8

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]

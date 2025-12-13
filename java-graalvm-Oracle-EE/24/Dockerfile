FROM --platform=$TARGETOS/$TARGETARCH rockylinux:9-minimal

LABEL author="DonPedroTV"
LABEL maintainer="admin@donpedrotv.com"
LABEL org.opencontainers.image.source="https://github.com/DonPedroTV/pterodactyl-images"
LABEL org.opencontainers.image.licenses="MIT"

RUN microdnf install -y \
    wget \
    ca-certificates \
    openssl \
    git \
    tar \
    sqlite \
    fontconfig \
    tzdata \
    iproute \
    gcc \
    gcc-c++ \
    freetype \
    libstdc++ \
    lsof \
    glibc-langpack-en \
    shadow-utils \
    && microdnf clean all

ARG TARGETARCH=amd64

RUN set -eux; \
  case "${TARGETARCH}" in \
    amd64)  URL="https://download.oracle.com/graalvm/24/latest/graalvm-jdk-24_linux-x64_bin.tar.gz" ;; \
    arm64)  URL="https://download.oracle.com/graalvm/24/latest/graalvm-jdk-24_linux-aarch64_bin.tar.gz" ;; \
    *) echo "Unsupported TARGETARCH: ${TARGETARCH}" >&2; exit 1 ;; \
  esac; \
  wget -O /tmp/graalvm.tar.gz "$URL"; \
  mkdir -p /opt/graalvm; \
  tar -xzf /tmp/graalvm.tar.gz --strip-components=1 -C /opt/graalvm; \
  rm -f /tmp/graalvm.tar.gz

RUN useradd -m -d /home/container container

ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8
ENV JAVA_HOME=/opt/graalvm
ENV PATH=/opt/graalvm/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh
CMD ["/bin/bash", "/entrypoint.sh"]

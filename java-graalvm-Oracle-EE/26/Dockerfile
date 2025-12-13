FROM --platform=$TARGETOS/$TARGETARCH debian:bookworm-slim

LABEL author="DonPedroTV"
LABEL maintainer="admin@donpedrotv.com"
LABEL org.opencontainers.image.source="https://github.com/DonPedroTV/pterodactyl-images"
LABEL org.opencontainers.image.licenses="MIT"

ARG TARGETARCH

# Pakiety w Debianie: apt, nie microdnf
RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
    ca-certificates \
    openssl \
    git \
    tar \
    sqlite3 \
    fontconfig \
    tzdata \
    iproute2 \
    libfreetype6 \
    libstdc++6 \
    lsof \
    locales \
    passwd \
    bash \
    && rm -rf /var/lib/apt/lists/*

# Locale (odpowiednik "glibc-langpack-en" z RHEL-świata)
RUN sed -i 's/^# *\(en_US.UTF-8\)/\1/' /etc/locale.gen && locale-gen

ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8

# GraalVM: dobierz architekturę do TARGETARCH
RUN set -eux; \
    case "${TARGETARCH}" in \
      amd64)  GRAAL_ARCH="x64" ;; \
      arm64)  GRAAL_ARCH="aarch64" ;; \
      *) echo "Unsupported arch: ${TARGETARCH}" && exit 1 ;; \
    esac; \
    wget -O /tmp/graalvm.tar.gz "https://github.com/graalvm/oracle-graalvm-ea-builds/releases/download/jdk-26.0.0-ea.06/graalvm-jdk-26.0.0-ea.06_linux-${GRAAL_ARCH}_bin.tar.gz"; \
    mkdir -p /opt/graalvm; \
    tar -xzf /tmp/graalvm.tar.gz --strip-components=1 -C /opt/graalvm; \
    rm /tmp/graalvm.tar.gz

RUN useradd -m -d /home/container container

ENV JAVA_HOME=/opt/graalvm
ENV PATH=/opt/graalvm/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh
CMD ["/bin/bash", "/entrypoint.sh"]

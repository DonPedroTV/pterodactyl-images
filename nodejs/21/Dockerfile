FROM node:21-bullseye-slim

LABEL author="DonPedroTV" maintainer="admin@donpedrotv.com"
LABEL org.opencontainers.image.source="https://github.com/DonPedroTV/pterodactyl-images"
LABEL org.opencontainers.image.licenses="MIT"

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Etc/UTC

RUN set -eux; \
    apt-get update; \
    apt-get -y install --no-install-recommends \
      curl ffmpeg iproute2 git sqlite3 python3 tzdata ca-certificates dnsutils build-essential locales; \
    sed -i 's/^# *\(en_US.UTF-8 UTF-8\)/\1/' /etc/locale.gen; \
    locale-gen; \
    npm install -g npm@latest; \
    apt-get clean; \
    rm -rf /var/lib/apt/lists/*; \
    useradd -m -d /home/container -s /bin/bash container

ENV LC_ALL=en_US.UTF-8
ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US.UTF-8

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh
CMD ["/bin/bash", "/entrypoint.sh"]

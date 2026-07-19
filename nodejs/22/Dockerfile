FROM        node:22-bullseye-slim

LABEL       author="Softwarenoob" maintainer="admin@softwarenoob.com"
LABEL       org.opencontainers.image.source="https://github.com/DonPedroTV/pterodactyl-images"
LABEL       org.opencontainers.image.licenses="MIT"

RUN         apt-get update || (sleep 15 && apt-get update) || (sleep 30 && apt-get update) \
            && apt-get -y install --no-install-recommends curl iproute2 git sqlite3 python3 tzdata ca-certificates dnsutils build-essential locales \
            && apt-get -y install --no-install-recommends --fix-missing ffmpeg || echo "Warning: ffmpeg installation failed, continuing without it" \
            && apt-get clean \
            && rm -rf /var/lib/apt/lists/* \
            && useradd -m -d /home/container container \
            && locale-gen en_US.UTF-8

ENV         LC_ALL=en_US.UTF-8
ENV         LANG=en_US.UTF-8
ENV         LANGUAGE=en_US.UTF-8

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]

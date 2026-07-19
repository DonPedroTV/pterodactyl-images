FROM node:17-bullseye-slim

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Etc/UTC

RUN set -eux; \
  sed -i 's|deb http://deb.debian.org/debian|deb [trusted=yes] http://archive.debian.org/debian|g' /etc/apt/sources.list; \
  sed -i 's|deb http://security.debian.org/debian-security|deb [trusted=yes] http://deb.debian.org/debian-security|g' /etc/apt/sources.list; \
  printf 'Acquire::Check-Valid-Until "false";\n' > /etc/apt/apt.conf.d/99no-check-valid; \
  apt-get update; \
  apt-get -y install --no-install-recommends \
    curl ffmpeg iproute2 git sqlite3 python3 tzdata ca-certificates dnsutils build-essential locales; \
  sed -i 's/^# *\(en_US.UTF-8 UTF-8\)/\1/' /etc/locale.gen; \
  locale-gen; \
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

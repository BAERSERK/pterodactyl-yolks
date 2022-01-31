FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-alpine

LABEL author="BAERSERK" maintainer="admin@baerserk.de"

RUN apk add --no-cache --update opus-dev youtube-dl ffmpeg

RUN adduser --disabled-password --home /home/container container

USER container
ENV USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/ash", "/entrypoint.sh"]

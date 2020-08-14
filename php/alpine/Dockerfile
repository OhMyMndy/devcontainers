FROM mcr.microsoft.com/vscode/devcontainers/base:alpine-3.12

RUN apk add --no-cache sudo less file vim iputils git bash

RUN apk add --no-cache php7-cli php7-pcntl php7-xml php7-curl php7-json php7-pecl-yaml php7-pdo php7-zip php7-dom php7-pecl-zmq php7-tokenizer php7-xmlwriter composer
RUN apk add --no-cache docker-cli docker-compose

ENV USERNAME=vscode
USER $USERNAME
RUN composer global require phpstan/phpstan
RUN composer global require phpunit/phpunit

RUN mkdir -p /home/$USERNAME/.vscode-server/extensions \
        /home/$USERNAME/.vscode-server-insiders/extensions \
    && chown -R $USERNAME \
        /home/$USERNAME/.vscode-server \
        /home/$USERNAME/.vscode-server-insiders
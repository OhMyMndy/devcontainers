FROM mcr.microsoft.com/vscode/devcontainers/base:alpine-3.12

ENV USERNAME=vscode



RUN apk add --no-cache git python3 py3-pip



USER $USERNAME

RUN pip install -U pylint --user

RUN mkdir -p /home/$USERNAME/.vscode-server/extensions \
        /home/$USERNAME/.vscode-server-insiders/extensions \
    && chown -R $USERNAME \
        /home/$USERNAME/.vscode-server \
        /home/$USERNAME/.vscode-server-insiders
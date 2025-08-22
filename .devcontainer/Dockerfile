# Image de base
FROM node:20-bullseye

# Installer SSHFS
RUN apt-get update && apt-get install -y sshfs fuse && rm -rf /var/lib/apt/lists/*

# Créer un utilisateur non-root
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME \
    && useradd -s /bin/bash --uid $USER_UID --gid $USER_GID -m $USERNAME \
    && apt-get update && apt-get install -y sudo \
    && echo "$USERNAME ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER $USERNAME
WORKDIR /workspace

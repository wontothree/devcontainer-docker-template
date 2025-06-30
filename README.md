# Ubuntu 22.04 Devcontainer + Docker Template

    devcontainer-docker-template
    └── .devcontainer
        ├── devcontainer.json
        ├── docker-compose.yml
        └── Dockerfile

# devcontainer.json

```json
{
  "name": "Ubuntu 22.04 Dev Container",
  "dockerComposeFile": "docker-compose.yml",
  "service": "ubuntu_dev",
  "workspaceFolder": "/workspace",
  "settings": {
    "terminal.integrated.shell.linux": "/bin/bash"
  },
  "extensions": [],
  "remoteUser": "root"
}
```

# docker-compose.yml

```yml
{
  "name": "Ubuntu 22.04 Dev Container",
  "dockerComposeFile": "docker-compose.yml",
  "service": "ubuntu_dev",
  "workspaceFolder": "/workspace",
  "settings": {
    "terminal.integrated.shell.linux": "/bin/bash"
  },
  "extensions": [],
  "remoteUser": "root"
}
```

# Dockerfile

```Dockerfile
# Docker Base Image
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# install basic package
RUN apt update && apt install -y \
    bash \
    sudo \
    vim \
    git \
    curl \
    build-essential \
    && rm -rf /var/lib/apt/lists/*
```
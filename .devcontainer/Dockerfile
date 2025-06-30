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

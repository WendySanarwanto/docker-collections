# ============================================================
# Pick base image from ubuntu:16.04 image
# ============================================================
FROM ubuntu:16.04
MAINTAINER Wendy Sanarwanto "wendy.sanarwanto@gmail.com"

# ============================================================
# Upgrade the ubuntu to latest LTS version 16.04.2 LTS
# And also install other required dependencies & softwares
# ============================================================
RUN apt-get update && apt-get upgrade -y && apt-get install -y build-essential \
    libssl-dev \
    nodejs \
    npm \
    software-properties-common \
    wget\
    vim

# ============================================================
# Rename `nodejs` command to `node` command.
# ============================================================
RUN update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10 && \
# ============================================================
# Upgrade the nodejs to LTS version
# ============================================================
    npm install -g n && \
    n lts && \
# ============================================================
# Upgrade the npm to latest one
# ============================================================
    npm install -g npm

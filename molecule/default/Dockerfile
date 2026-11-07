FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        python3 \
        sudo \
        systemctl \
        net-tools \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

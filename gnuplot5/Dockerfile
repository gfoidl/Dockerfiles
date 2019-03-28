# Docker image for gnuplot5

# Maintainer gfoidl, 2019

# ubuntu is smaller than debian
FROM ubuntu

RUN apt update \
&&  apt install -y gnuplot5 \
&&  rm -rf /var/lib/apt/lists/* /tmp/*

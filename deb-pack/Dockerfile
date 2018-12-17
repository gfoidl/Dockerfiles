# ubuntu is smaller than debian
FROM ubuntu

# dh_make needs the $USER
ENV USER root

RUN apt update \
&&  apt install -y dh-make \
&&  rm -rf /var/lib/apt/lists/*

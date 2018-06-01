# Docker image for .net Core SDK 2.1 + libxml2

# Maintainer gfoidl, 2018

FROM microsoft/dotnet:2.1-sdk

RUN	apt-get update \
&&	apt-get install -y libxml2-utils \
&&	rm -rf /var/lib/apt/lists/* /tmp/*

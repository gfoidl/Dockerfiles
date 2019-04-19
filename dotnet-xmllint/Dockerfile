# Docker image for .NET Core SDK 3.0 + 2.1 runtime + libxml2

# Maintainer gfoidl, 2018-2019

FROM gfoidl/dotnet-ci:sdk3.0-runtime2.1

RUN	apt-get update \
&&	apt-get install -y libxml2-utils \
&&	rm -rf /var/lib/apt/lists/* /tmp/*

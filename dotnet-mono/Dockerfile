# Docker image for .net Core SDK 2.0 + mono 5.4.0.201

# Maintainer gfoidl, 2017

FROM microsoft/dotnet:2.0.0-sdk

ENV MONO_VERSION            5.4.0.201

# https://github.com/dotnet/netcorecli-fsc/wiki/.NET-Core-SDK-1.0#using-net-framework-as-targets-framework-the-osxunix-build-fails
ENV FrameworkPathOverride   /usr/lib/mono/4.6.1-api

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF \
&&  echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list \
&&  apt-get update \
&&  apt-get install -y binutils curl mono-devel ca-certificates-mono nuget referenceassemblies-pcl  \
&&  rm -rf /var/lib/apt/lists/* /tmp/*

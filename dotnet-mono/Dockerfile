# Docker image for .net Core SDK 2.2 + mono 5.18.1.0

# Maintainer gfoidl, 2017-2019

FROM microsoft/dotnet:2.2-sdk

ENV MONO_VERSION            5.18.1.0

# https://github.com/dotnet/netcorecli-fsc/wiki/.NET-Core-SDK-1.0#using-net-framework-as-targets-framework-the-osxunix-build-fails
ENV FrameworkPathOverride   /usr/lib/mono/4.7.1-api

RUN apt update \
&&  apt install -y apt-transport-https dirmngr \
&&  apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF \
&&  echo "deb https://download.mono-project.com/repo/debian stable-stretch/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list \
&&  apt update \
&&  apt install -y binutils curl mono-devel ca-certificates-mono nuget referenceassemblies-pcl  \
&&  rm -rf /var/lib/apt/lists/* /tmp/*

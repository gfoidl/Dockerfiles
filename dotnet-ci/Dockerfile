# Docker image for .NET Core 3.0 SDK + .NET Core 2.2 Runtime + .NET Core 2.1 Runtime

# Maintainer gfoidl, 2019

FROM mcr.microsoft.com/dotnet/core/sdk:3.0

RUN apt update \
&&  apt install -y apt-transport-https \
&&  wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.asc.gpg \
&&  mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/ \
&&  wget -q https://packages.microsoft.com/config/debian/9/prod.list \
&&  mv prod.list /etc/apt/sources.list.d/microsoft-prod.list \
&&  apt update \
&&  apt install -y aspnetcore-runtime-2.2 aspnetcore-runtime-2.1 \
&&  rm -rf /var/lib/apt/lists/* /tmp/*

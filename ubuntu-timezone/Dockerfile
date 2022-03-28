# ubuntu is smaller than debian
FROM mcr.microsoft.com/dotnet/runtime-deps:6.0-focal

ENV TZ=Europe/Vienna

# Cf. https://gist.github.com/sidja/833eb9824ada2684773553824f28e910
RUN apt update \
&&  DEBIAN_FRONTEND=noninteractive apt install tzdata \
&&  ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
&&  echo $TZ > /etc/timezone \
&&  dpkg-reconfigure --frontend noninteractive tzdata \
&&  rm -rf /var/lib/apt/lists/*

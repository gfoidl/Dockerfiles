# Docker image for .net Core SDK 2.1 + CircleCI Node-Jessie-Browsers 10.13.0 + trx2junit

# Maintainer gfoidl, 2018

FROM circleci/node:10-jessie-browsers

ENV KW_UI_TEST_CHROME 1
ENV KW_UI_TEST_DRIVER_DIR /tmp

# https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-current
# first two commands (first line) are needed for user/root rights in circleci/node-images, sure there will be a better way...
RUN sudo touch microsoft.asc.gpg && sudo chown $(whoami) microsoft.asc.gpg \
&&  wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.asc.gpg \
&&  sudo mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/ \
&&  sudo wget -q https://packages.microsoft.com/config/debian/8/prod.list \
&&  sudo mv prod.list /etc/apt/sources.list.d/microsoft-prod.list \
&&  sudo apt install apt-transport-https \
&&  sudo apt update \
&&  sudo apt install dotnet-sdk-2.1 \
&&  sudo rm -rf /var/lib/apt/lists/* /tmp/* \
&&  dotnet tool install -g trx2junit

# Chrome webdriver
RUN sudo curl -o /tmp/chromedriver.zip https://chromedriver.storage.googleapis.com/2.43/chromedriver_linux64.zip \
&&  sudo unzip /tmp/chromedriver.zip -d /tmp \
&&  sudo rm /tmp/chromedriver.zip

FROM ubuntu:16.04
MAINTAINER Elias Baryshnikov <qwelias@gmail.com>
LABEL version='2.0.0'

RUN apt update
run apt install -y curl wget
# NodeJS
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -

# install
RUN apt update
RUN apt install -y nodejs \
    python \
    libkrb5-dev \
    libcairo2-dev \
    libjpeg8-dev \
    libpango1.0-dev \
    libgif-dev \
    build-essential \
    g++

# PM2
RUN npm i -g pm2

# GitBook
RUN npm install -g gitbook-cli
RUN wget -nv -O- https://raw.githubusercontent.com/kovidgoyal/calibre/master/setup/linux-installer.py | python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"

CMD

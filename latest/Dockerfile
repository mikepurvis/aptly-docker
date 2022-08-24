FROM debian:stretch
MAINTAINER Mike Purvis

RUN apt-get update && \
apt-get install gnupg -y && \
apt-get clean


# Instructions from: http://www.aptly.info/download/
RUN echo "deb http://repo.aptly.info/ squeeze main" > /etc/apt/sources.list.d/aptly.list && \
apt-key adv --keyserver keyserver.ubuntu.com --recv-keys A0546A43624A8331 && \
apt-get update && \
apt-get install aptly ca-certificates -y && \
apt-get clean

ADD aptly.conf /etc/aptly.conf
VOLUME ["/aptly"]

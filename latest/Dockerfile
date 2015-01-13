FROM debian:jessie
MAINTAINER Mike Purvis

# Instructions from: http://www.aptly.info/download/
RUN echo "deb http://repo.aptly.info/ squeeze main" > /etc/apt/sources.list.d/aptly.list; \
apt-key adv --keyserver keys.gnupg.net --recv-keys 2A194991; \
apt-get update; \
apt-get install aptly -y

ADD aptly.conf /etc/aptly.conf
VOLUME ["/aptly"]

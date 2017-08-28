FROM debian:stable
MAINTAINER Lachlan de Waard <dockerlachlan@dewaard.email>

ADD playlist.m3u /etc/
ADD ezstream_mp3.xml /etc/

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --install-recommends ezstream && rm -rf /var/lib/apt/lists/* 

CMD /usr/bin/ezstream -c /etc/ezstream_mp3.xml

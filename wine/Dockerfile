FROM debian:jessie

RUN apt-get update && \
    apt-get install -y wine \
	--no-install-recommends && \
	dpkg --add-architecture i386 && \
	apt-get update && \
	apt-get install -y \
	wine32 \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

RUN mkdir /home/wine && \
	groupadd -g 1000 wine && \
    useradd -u 1000 -g 1000 \
	wine --home /home/wine && \
	chown -R wine:wine /home/wine

WORKDIR /home/wine
USER wine
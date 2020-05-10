FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt-get install -y software-properties-common \
		&& add-apt-repository ppa:nilarimogard/webupd8 -y \
		&& apt install -y ffmpeg streamlink \
		&& apt clean

COPY ffserver.conf /etc/
COPY stream2rtsp /usr/bin/

EXPOSE 5554

ENTRYPOINT  ["/usr/bin/stream2rtsp"]

FROM ubuntu

RUN apt-get update && apt-get install -y rtorrent \
&& mkdir /root/files \
&& mkdir /root/torrents

COPY rtorrent.rc /root/.rtorrent.rc
COPY ./download.sh /root/torrents/download.sh
COPY ./clear.sh /root/torrents/clear.sh

RUN chmod u+x /root/torrents/clear.sh /root/torrents/download.sh\
&& mkdir ~/rtorrent_Download_Files \
&& mkdir ~/rtorrent_session \
&& mkdir ~/rtorrent_Watch \
&& mkdir ~/rtorrent_FullDownload_Files 

VOLUME /root/files
VOLUME /root/torrents

WORKDIR /root/torrents

CMD ["bash"]

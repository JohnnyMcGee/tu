FROM ubuntu

RUN apt update && apt-get install -y rtorrent \
&& mkdir /root/files \
&& mkdir /root/torrents

COPY rtorrent.rc /root/.rtorrent.rc

RUN mkdir ~/rtorrent_Download_Files \
&& mkdir ~/rtorrent_session \
&& mkdir ~/rtorrent_Watch \
&& mkdir ~/rtorrent_FullDownload_Files 

VOLUME /root/files
VOLUME /root/torrents

WORKDIR /root/torrents

CMD ["bash"]
FROM python

RUN pip3 install pirate-get \
&& mkdir /root/torrents \
&& echo "alias pg='pirate-get'" >> /root/.bashrc

WORKDIR /root/torrents

VOLUME /root/torrents

CMD ["bash"]
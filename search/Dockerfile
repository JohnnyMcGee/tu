FROM python

RUN pip3 install pirate-get \
&& mkdir /root/torrents \
&& mkdir /root/.config \
&& echo "alias pg='pirate-get'" >> /root/.bashrc

COPY pirate-get /root/.config

WORKDIR /root/torrents

VOLUME /root/torrents

CMD ["bash"]
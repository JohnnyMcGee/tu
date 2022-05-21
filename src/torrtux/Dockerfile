FROM perl

WORKDIR /root/ 

COPY torrtux /root/torrtux
COPY torrtuxrc /root/.torrtuxrc

WORKDIR /root/torrtux/

RUN apt-get update && apt install -y xclip
RUN apt-get install -y xclip cpanminus

# Install modules with cpan
RUN cpanm IO::Uncompress::Gunzip \
&& cpanm LWP \
&& cpanm HTML::TreeBuilder \
&& cpanm AppConfig \
&& cpanm Term::ANSIColor \
&& cpanm XML::RPC \
&& cpanm XML/RPC.pm

RUN apt install -y libwww-perl  libswitch-perl librpc-xml-perl
RUN perl install.pl
RUN mkdir /root/torrents 

WORKDIR /root/torrents

VOLUME /root/torrents

CMD ["bash"]
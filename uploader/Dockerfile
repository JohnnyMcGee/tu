FROM golang

RUN go install github.com/prasmussen/gdrive@latest \
&& mkdir /root/files

WORKDIR /root/files

COPY ./cred.json /root/.gdrive/cred.json
COPY ./upload.sh /root/files/
COPY ./clear.sh /root/files/

VOLUME /root/files

CMD ["bash"]
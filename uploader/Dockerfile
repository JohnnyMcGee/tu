FROM golang

RUN go install github.com/prasmussen/gdrive@latest \
&& mkdir /root/files

WORKDIR /root/files

COPY ./cred.json /root/.gdrive/cred.json

VOLUME /root/files

CMD ["bash"]
FROM golang

RUN go install github.com/prasmussen/gdrive@latest \
&& mkdir /root/files
# directory to upload files from

COPY ./upload.sh /root/files/
COPY ./clear.sh /root/files/

WORKDIR /root/files

VOLUME /root/files

CMD ["bash"]
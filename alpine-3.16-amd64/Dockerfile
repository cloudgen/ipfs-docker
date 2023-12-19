FROM alpine:3.16
LABEL maintainer="Cloudgen Wong <cloudgen.wong@theauthority.asia>" \
   architecture="amd64/x86_64"

ADD target/lib.tar.gz /
ADD target/lib64.tar.gz /
ADD target/usr.tar.gz /
ADD target/root.tar.gz /

RUN /bin/sh -c "chown root:root -R /root && chown root:root -R /usr && chown root:root -R /lib && chown root:root -R /lib64"

WORKDIR /data
EXPOSE 4001 8080 5001
VOLUME ["/data"]
ENTRYPOINT ["/usr/local/bin/start-container"]

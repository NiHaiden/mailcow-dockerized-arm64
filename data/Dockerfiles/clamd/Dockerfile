FROM niklashaiden/clamav-aarch64

LABEL maintainer "André Peters <andre.peters@servercow.de>"

RUN apk upgrade --no-cache \
  && apk add --update --no-cache \
  rsync \
  bind-tools \
  bash 

COPY clamd.sh ./
RUN chmod +x /sbin/tini

ENTRYPOINT []
CMD ["/sbin/tini", "-g", "--", "/clamd.sh"]

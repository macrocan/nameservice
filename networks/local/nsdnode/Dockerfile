FROM ubuntu:16.04

RUN apt-get update && \
    apt-get -y upgrade && \
    apt-get -y install curl jq file

VOLUME [ /nsd ]
WORKDIR /nsd
EXPOSE 26656 26657
ENTRYPOINT ["/usr/bin/wrapper.sh"]
CMD ["start"]
STOPSIGNAL SIGTERM

COPY wrapper.sh /usr/bin/wrapper.sh


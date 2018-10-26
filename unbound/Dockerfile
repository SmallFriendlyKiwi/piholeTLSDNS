FROM arm32v6/alpine:latest
EXPOSE 53/udp
RUN apk add --update --no-cache -q --progress unbound && \
    rm -rf /etc/unbound/unbound.conf /var/cache/apk/*
COPY unbound.conf /etc/unbound/unbound.conf
ENTRYPOINT unbound -d

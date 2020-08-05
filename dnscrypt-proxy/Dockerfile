FROM alpine:latest

RUN apk add --no-cache wget tar && \
 wget https://github.com/DNSCrypt/dnscrypt-proxy/releases/download/2.0.39/dnscrypt-proxy-linux_x86_64-2.0.39.tar.gz && \
 tar xzf dnscrypt-proxy-linux_x86_64-2.0.39.tar.gz && \
 mv linux-x86_64/dnscrypt-proxy . && \
 mv linux-x86_64/example-dnscrypt-proxy.toml dnscrypt-proxy.toml && \
 rm -rf linux-x86_64/ dnscrypt-proxy-linux_x86_64-2.0.39.tar.gz && \
 sed -i "s/listen_addresses = \['127\.0\.0\.1:53'\]/listen_addresses = [':53']/g" dnscrypt-proxy.toml

EXPOSE 53/tcp 53/udp

CMD ./dnscrypt-proxy

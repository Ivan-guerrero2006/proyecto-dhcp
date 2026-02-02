FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install -y isc-dhcp-server net-tools iproute2 && \
    apt clean

COPY ../config/dhcpd.conf /etc/dhcp/dhcpd.conf

CMD ["dhcpd", "-4", "-f", "-d"]

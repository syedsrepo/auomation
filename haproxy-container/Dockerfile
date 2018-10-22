FROM local:haproxy-base
LABEL description = "haproxy image with collectd"
RUN apt update -y
RUN apt install net-tools
RUN apt install netcat

RUN apt install haproxy -y
COPY haproxy.cfg /etc/haproxy/haproxy.cfg

COPY docker-entrypoint.sh /usr/local/bin/
COPY startup.sh   /usr/local/bin/


ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["startup.sh"]

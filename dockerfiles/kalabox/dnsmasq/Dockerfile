# Dnsmasq image for wildcard support *.kbox
# docker build -t kalabox/dnsmasq .
# docker run -d -p 1.3.3.7:53:53/udp --name dnsmasq kalabox/dnsmasq

FROM kalabox/debian

RUN apt-get install -y dnsmasq && apt-get clean

RUN echo 'user=root' >> /etc/dnsmasq.conf
RUN echo 'address=/.kbox/1.3.3.7' >> /etc/dnsmasq.conf

EXPOSE 53

CMD ["/usr/sbin/dnsmasq", "-d"]

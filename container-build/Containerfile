FROM docker.io/library/httpd
RUN \
sed -i "s/Listen 80/Listen 8080/g" \
      /etc/httpd/conf/httpd.conf && \
sed -i "s/#ServerName www.example.com:80/ServerName 0.0.0.0:8080/g  \
      /etc/httpd/conf/httpd.conf"
RUN \
chown -R 0 /var/log/httpd /var/run/httpd && \
chmod -R g=u /var/log/httpd /var/run/httpd
EXPOSE 8080
USER 1001

FROM prestashop/prestashop:1.7-7.2-apache


COPY custom.ini /usr/local/etc/php/conf.d/
COPY uploads.ini /usr/local/etc/php/conf.d/
#COPY ssl-cert-snakeoil.pem /etc/ssl/certs/
#COPY ssl-cert-snakeoil.key /etc/ssl/private/
#COPY mkcertRootCA.crt /usr/local/share/ca-certificates/
#RUN update-ca-certificates
#RUN a2enmod ssl
#RUN a2ensite default-ssl
RUN apt-get update && apt-get install -y libmemcached-dev
RUN yes '' | pecl install -f mcrypt memcached

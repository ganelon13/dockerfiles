FROM php:7.0-apache

COPY entrypoint.sh /entrypoint.sh

RUN chmod +x /entrypoint.sh && \
    mkdir -p /opt/src && \
    curl https://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz --output /opt/src/dokuwiki.tgz && \
    cd /opt/src/ && \
    tar zxf dokuwiki.tgz && \
    rm -f dokuwiki.tgz && \
    mv dokuwiki* dokuwiki && \
    rm -fr /var/www/html && \
    cp -R dokuwiki /var/www/html && \
    chown -R www-data /var/www/html

EXPOSE 80 443
VOLUME ["/var/www/html/data", "/var/www/html/lib"]

CMD ["/entrypoint.sh"]

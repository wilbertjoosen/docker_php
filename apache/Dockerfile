FROM webdevops/apache:ubuntu-16.04

MAINTAINER Eric Pfeiffer <computerfr33k@users.noreply.github.com>

ARG PHP_SOCKET=php:9000

ENV WEB_PHP_SOCKET=php:9000

ENV WEB_DOCUMENT_ROOT=/var/www/

EXPOSE 80 443

WORKDIR /var/www/

RUN touch /var/log/php-errors.log
RUN chown www-data:www-data /var/log/php-errors.log

ADD vhost.conf /etc/apache2/sites-enabled/vhost.conf

ENTRYPOINT ["/opt/docker/bin/entrypoint.sh"]

CMD ["supervisord"]
FROM alpine:latest

RUN echo "http://dl-cdn.alpinelinux.org/alpine/v3.5/main/" > /etc/apk/repositories

RUN apk --update --no-cache add ca-certificates nginx curl
RUN apk add php5 php5-xml php5-exif php5-fpm php5-soap php5-openssl php5-gmp php5-pdo_odbc php5-json php5-dom php5-pdo php5-zip php5-mysqli php5-sqlite3 php5-pdo_pgsql php5-bcmath php5-gd php5-odbc php5-pdo_mysql php5-pdo_sqlite php5-gettext php5-xmlreader php5-bz2 php5-iconv php5-pdo_dblib php5-curl php5-ctype php5-phar

RUN curl -sS https://getcomposer.org/installer -o composer-setup.php
RUN /usr/bin/php5 composer-setup.php --install-dir=/usr/local/bin --filename=composer
RUN rm -rf composer-setup.php

USER container
ENV  USER container
ENV HOME /home/container

WORKDIR /home/container
COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/ash", "/entrypoint.sh"]

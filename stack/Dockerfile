FROM debian:stretch

RUN apt update && apt install -y nginx php7.0 php7.0-fpm php7.0-mbstring php7.0-mcrypt php7.0-mysql php7.0-gd
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN usermod -u 1000 www-data
RUN service php7.0-fpm start

CMD service php7.0-fpm start && /usr/sbin/nginx -g "daemon off;"

EXPOSE 80
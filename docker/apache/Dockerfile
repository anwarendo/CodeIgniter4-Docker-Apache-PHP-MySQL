FROM ubuntu:22.04

RUN apt-get update -y && \
    apt-get install tzdata -y && \
    apt-get install apache2 -y && \
    apt-get install nano -y 

RUN apt-get install -y software-properties-common \
    && add-apt-repository ppa:ondrej/php \ 
    && apt-get update -y \ 
    && apt-get install -y \
    php7.4 \
    php7.4-cli \
    php7.4-fpm \
    # php7.2-opcache \
    libapache2-mod-php7.4  \
    php7.4-common \
    php7.4-bcmath \
    php-json \
    php7.4-mbstring \
    php7.4-tokenizer \
    php7.4-xml \
    php7.4-zip \
    php7.4-soap \
    php7.4-mysql \
    php7.4-curl \ 
    php7.4-intl

WORKDIR /var/www/html


ENTRYPOINT [ "apachectl", "-D", "FOREGROUND"]
FROM php:7.3.6

# disable interactive functions
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
    apt-get install -y \
    zip \
    unzip \
    libzip-dev \
    libpng-dev \
    libxml2-dev \
    libxslt1-dev \
    python-pip

RUN pip install awscli --upgrade

RUN docker-php-ext-configure zip --with-libzip

RUN docker-php-ext-install \
    mbstring \
    zip \
    gd \
    bcmath \
    xml \
    intl \
    soap \
    xsl \
    pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

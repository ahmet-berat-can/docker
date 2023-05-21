# ana imajı belirleme
FROM php:7.3-apache 

# Base imaj OS update etme
RUN apt-get update -y && apt-get install mariadb-client -y

# Docker php modülü install etme
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

# imaj için klasör olusturma
RUN mkdir /var/www/html/images

# Klasör yetkilendirmesi
RUN chmod 777 /var/www/html/images

# php klasörü altındakileri container'ın folder'ına kopyalama
COPY ./php/ /var/www/html/
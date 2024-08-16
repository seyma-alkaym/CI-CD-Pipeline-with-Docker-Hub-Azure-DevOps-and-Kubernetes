# PHP 7.3 sürümünü baz alan resmi PHP Apache görüntüsünü kullanýyoruz
FROM php:7.3.33-apache

# Apache mod_rewrite modülünü etkinleþtiriyoruz (URL yeniden yazýmý için gereklidir)
RUN a2enmod rewrite

# PHP eklenti gereksinimlerini kuruyoruz (örneðin: mysqli, pdo_mysql gibi)
RUN docker-php-ext-install mysqli pdo_mysql

# Çalýþma dizinini /var/www/html/caiwl altýna ayarlýyoruz
WORKDIR /var/www/html/boat

# Lokal projenizin dosyalarýný Docker görüntüsüne kopyalýyoruz
COPY . .

# Docker konteynerý açýldýðýnda Apache'yi baþlatýyoruz
CMD ["apache2-foreground"]

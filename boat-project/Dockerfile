# Using the official PHP Apache image based on PHP 7.3 version
FROM php:7.3.33-apache

# Enable Apache mod_rewrite module (required for URL rewriting)
RUN a2enmod rewrite

# Install PHP extension requirements (e.g., mysqli, pdo_mysql)
RUN docker-php-ext-install mysqli pdo_mysql

# Set the working directory to /var/www/html/boat
WORKDIR /var/www/html/boat

# Copy the files of your local project into the Docker image
COPY . .

# Start Apache when the Docker container starts
CMD ["apache2-foreground"]

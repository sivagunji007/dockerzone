FROM ubuntu:18.04
LABEL author ="Siva Gunji"
LABEL Organisation="Quality Thoughts"
RUN apt update && apt-get install apache2 -y
HEALTHCHECK CMD [ "curl -f http://localhost/ || exit 1" ]
VOLUME [ "var/www/html" ]
EXPOSE 80
CMD ["apache2ctl","-D","FOREGROUND"]
FROM ubuntu:14.04
MAINTAINER Aleksandr Volochnev <a.volochnev@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y nano apache2 php5

RUN rm -v /etc/apache2/sites-enabled/000-default.conf
#RUN sed -i "s/Listen 80/Listen 8080/" /etc/apache2/ports.conf
ADD app.conf /etc/apache2/sites-enabled/
ADD index.php /var/www/app/

EXPOSE 80

CMD /usr/sbin/apache2ctl -D FOREGROUND

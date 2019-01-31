FROM debian:latest
MAINTAINER veto<veto@myridia.com>
RUN apt-get update && apt-get install -y \
  apache2 \
  apt-transport-https \ 
  #ca-certificates \
  apt-utils \
  #openssh-server \
  supervisor 







RUN mkdir -p /var/lock/apache2 /var/run/apache2 /var/run/sshd /var/log/supervisor; \
a2enmod rewrite ssl; \
sed -i -e '/AllowOverride / s/ .*/ All/' /etc/apache2/apache2.conf; \
mkdir -p /var/lock/apache2 /var/run/apache2 /var/run/sshd /var/log/supervisor 

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
EXPOSE 22 80
CMD ["/usr/bin/supervisord"]



FROM ubuntu:18.04
MAINTAINER ziippy
LABEL "purpose"="my-nginx"
RUN apt-get update && \
apt-get install vim net-tools curl nginx -y && \
echo "\ndaemon off;" >> /etc/nginx/nginx.conf
RUN mkdir /var/www/html/gettime && \
mkdir /var/www/html/getrandom
COPY gettime/index.html /var/www/html/gettime/
COPY getrandom/index.html /var/www/html/getrandom
COPY default /etc/nginx/sites-enabled/
EXPOSE 80
WORKDIR /etc/nginx
CMD ["nginx"]

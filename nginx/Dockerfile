FROM centos:centos7

# Configure my repo to use my custom Nginx with modsec
RUN mkdir -p /usr/local/src
RUN cd /usr/local/src
RUN yum -y install wget vim htop tar

RUN yum install epel-release -y
# install nginx
RUN yum -y install nginx

# tell Nginx to stay foregrounded
ADD nginx.conf /etc/nginx/nginx.conf
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN mkdir -p /var/www
RUN curl https://git.centos.org/sources/httpd/c7/acf5cccf4afaecf3afeb18c50ae59fd5c6504910 \
| tar -xz -C /var/www \
--strip-components=1
RUN sed -i -e 's/Apache/nginx/g' -e '/apache_pb.gif/d' \
/var/www/index.html

# expose HTTP
EXPOSE 80
EXPOSE 8080
EXPOSE 443

# Run
CMD [ "/usr/sbin/nginx" ]

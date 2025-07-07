FROM redhat/ubi8

RUN yum -y install httpd && yum clean all

COPY . /var/www/html

EXPOSE 80

CMD ["/usr/sbin/httpd","-DFOREGROUND"]

# Simple Container
ARG TAGVERSION=6
FROM centos:${TAGVERSION}
LABEL maintainer="Ankit1.Sambhare@ril.com"

ENV http_proxy=http://10.159.0.3:8678
ENV https_proxy=http://10.159.0.3:8678

RUN yum update -y && \
    yum install -y httpd net-tools 
#    echo "This is Ankit Sambhare's containers" >> /var/www/html/index.html

COPY index.html  /var/www/html/
EXPOSE 80

ENTRYPOINT apachectl -DFOREGROUND

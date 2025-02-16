FROM httpd:latest
COPY httpd.conf /usr/local/apache2/conf/httpd.conf
COPY ssl/httpd-ssl.conf /usr/local/apache2/conf/extra/httpd-ssl.conf
COPY ssl/server.crt /usr/local/apache2/conf/server.crt
COPY ssl/server.key /usr/local/apache2/conf/server.key
COPY ssl/rootCA.crt /usr/local/apache2/conf/rootCA.crt

EXPOSE 443
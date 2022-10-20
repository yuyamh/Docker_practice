FROM ubuntu:22.04

ENV APACHE_CONFDIR=/etc/apache2
ENV APACHE_ENVVARS=$APACHE_CONFDIR/envvars

RUN apt update \
  && apt install -y apache2

#apacheはデフォルトで/var/www/html/以下のファイルを読み込みに行く。
#トップページに直接アクセスしたとき(localhost:8070)は、/var/www/html/以下にあるindex.htmlを読み込む仕様になっている。
COPY index.html /var/www/html/

CMD ["apachectl", "-D", "FOREGROUND"]

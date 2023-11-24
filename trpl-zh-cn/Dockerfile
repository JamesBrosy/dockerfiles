FROM httpd:latest
RUN apt update \
    && apt install -y git \
    && git clone -b gh-pages https://github.com/KaiserY/trpl-zh-cn.git /usr/local/apache2/htdocs/
EXPOSE 80

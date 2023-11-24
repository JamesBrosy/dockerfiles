FROM httpd:latest
RUN apt update \
    && apt install -y git \
    && git clone https://github.com/mmp/pbr-book-website /usr/local/apache2/htdocs/
EXPOSE 80

FROM httpd:latest
WORKDIR /usr/local/apache2/htdocs/
RUN apt update \
    && apt install -y git \
    && rm -rf ./* \
    && git clone https://github.com/mmp/pbr-book-website ./
EXPOSE 80

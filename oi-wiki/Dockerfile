FROM httpd:latest
RUN apt update \
    && apt install -y git \
    && git clone -b gh-pages https://github.com/OI-wiki/OI-wiki /usr/local/apache2/htdocs/

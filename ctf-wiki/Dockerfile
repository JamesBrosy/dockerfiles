FROM httpd:latest
WORKDIR /usr/local/apache2/htdocs/
RUN apt update \
    && apt install -y git \
    && rm -rf ./* \
    && git clone -b gh-pages https://github.com/ctf-wiki/ctf-wiki.git ./
EXPOSE 80

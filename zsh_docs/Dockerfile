FROM httpd:latest
RUN apt update \
    && apt install -y wget \
    && wget -qO- https://zsh.sourceforge.io/Doc/zsh_html.tar.gz | tar -zxvf - -C /usr/local/apache2/htdocs --strip-components 1
EXPOSE 80

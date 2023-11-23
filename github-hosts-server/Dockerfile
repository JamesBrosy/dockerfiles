FROM ubuntu:latest
RUN apt upate \
    && apt install -y curl \
    && curl -L https://github.com/ineo6/hosts/releases/download/v1.0.1/hosts-server-pkg-linuxstatic-x64.tar.gz | tar zxvf - -C /usr/bin --strip-components 2
CMD ["hosts-server", "-p", "8080"]

FROM ubuntu:latest
RUN apt update \
    && apt install -y python3 git
RUN git clone https://github.com/mmp/pbr-book-website /pbr-book-website
WORKDIR /pbr-book-website
CMD ["python3", "-m", "http.server", "8200"]

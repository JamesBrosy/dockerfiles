FROM rust:latest
ENV RUSTUP_UPDATE_ROOT=https://mirrors.ustc.edu.cn/rust-static/rustup \
    RUSTUP_DIST_SERVER=https://mirrors.ustc.edu.cn/rust-static
RUN rustup install 1.74.0-x86_64-unknown-linux-gnu \
    && rustup default 1.74.0-x86_64-unknown-linux-gnu \
    && rustup uninstall 1.57.0-x86_64-unknown-linux-gnu
RUN echo "[source.crates-io]\nreplace-with = 'rsproxy-sparse'" >> /usr/local/cargo/config.toml \
    && echo "[source.rsproxy-sparse]\nregistry = \"sparse+https://rsproxy.cn/index/\"" >> /usr/local/cargo/config.toml
RUN cargo install simple-http-server mdbook \
    && git clone https://github.com/KaiserY/trpl-zh-cn.git /trpl-zh-cn
WORKDIR /trpl-zh-cn
RUN mdbook build
CMD ["simple-http-server", "./book/html/", "-i", "-p", "8100"]

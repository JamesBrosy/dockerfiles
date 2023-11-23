FROM ubuntu:latest
RUN apt update \
    && apt install -y python3 python3-pip git \
    && git clone https://github.com/data-8/textbook.git /textbook \
    && pip3 config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple \
    && python3 -m pip install --upgrade pip
WORKDIR /textbook
RUN pip3 install jupyter-book \
    && jupyter-book build .
CMD ["python3", "-m", "http.server", "-d", "_build/html", "8300"]

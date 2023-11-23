FROM jupyterhub/jupyterhub
RUN pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple \
    && python3 -m pip install --upgrade pip \
    && mkdir /root/jupyter\ notebook
RUN python3 -m pip install jupyterlab notebook datascience
RUN apt update \
 && apt install vim git -y \
 && git clone https://github.com/data-8/materials-fa23.git

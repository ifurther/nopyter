FROM dclong/jupyterlab

RUN npm install -g configurable-http-proxy \
    && pip3 install jupyterhub \
    && /scripts/sys/purge_cache.sh \
    && npm cache clean --force

ADD settings/jupyter_server_config.py /etc/jupyter/
ADD settings/jupyterhub_config.py /etc/jupyterhub/
ADD scripts /scripts

EXPOSE 8000

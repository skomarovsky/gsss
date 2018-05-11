FROM  gettyimages/spark

RUN apt-get -y update && \
    pip --no-cache-dir install jupyter && \
    pip install https://dist.apache.org/repos/dist/dev/incubator/toree/0.2.0-incubating-rc3/toree-pip/toree-0.2.0.tar.gz && \
    jupyter toree install --spark_home=/usr/spark-2.3.0 && \
    pip install notebook && \
    jupyter notebook --generate-config
RUN sed -i s/#c.NotebookApp.ip = 'localhost'/c.NotebookApp.ip = '0.0.0.0'/g ~/.jupyter/jupyter_notebook_config.py
EXPOSE 8888
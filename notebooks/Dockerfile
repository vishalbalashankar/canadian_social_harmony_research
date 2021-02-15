FROM jupyter/datascience-notebook

EXPOSE 8875

RUN conda install --quiet --yes plotly pyvis networkx && \
    jupyter labextension install jupyterlab-plotly --no-build && \
    jupyter lab build -y && \
    jupyter lab clean -y

COPY requirements.txt /

RUN pip install -r /requirements.txt
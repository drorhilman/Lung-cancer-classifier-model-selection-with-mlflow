# hash:sha256:6567a215aa8492a0d962e73986b3fc53946d01bab9db98300c886fd8987fc063
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:22.11.1-4-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y \
        jupyterlab \
    && conda clean -ya

RUN mamba install -y \
        mlflow==2.16.2 \
        pandas==2.2.3 \
        scikit-learn==1.5.2 \
        xgboost==2.1.1 \
    && mamba clean -ya

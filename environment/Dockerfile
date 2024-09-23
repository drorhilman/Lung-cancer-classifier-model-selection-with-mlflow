# hash:sha256:085400fbc8ae215be6c1bfac22ced009e9ebc9f4037414b3f168f8228703e027
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:22.11.1-4-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y \
        jupyterlab==4.2.5 \
    && conda clean -ya

RUN mamba install -y \
        mlflow==2.16.2 \
        pandas==2.2.3 \
        scikit-learn==1.5.2 \
        xgboost==2.1.1 \
    && mamba clean -ya

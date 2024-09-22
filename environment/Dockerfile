# hash:sha256:99ce16e1b16a7776b4fe396a4ced62a4d727f8cf62e5f86aef33badeee7859f3
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:22.11.1-4-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN mamba install -y \
        mlflow==2.16.2 \
        pandas==2.2.3 \
        scikit-learn==1.5.2 \
        xgboost==2.1.1 \
    && mamba clean -ya

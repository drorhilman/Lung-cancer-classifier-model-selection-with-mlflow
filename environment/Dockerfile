# hash:sha256:ae0082a0b6215359de94a695c7853d1dafadd46bd37ff589cef4b70f6939f915
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/mambaforge3:22.11.1-4-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN mamba install -y \
        mlflow \
        pandas \
        scikit-learn \
        xgboost \
    && mamba clean -ya

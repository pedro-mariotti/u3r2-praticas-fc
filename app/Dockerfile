# Etapa 1 (builder)
FROM ubuntu:latest AS builder
ARG GIT_TOKEN

RUN apt-get update && apt-get install -y git
RUN git config --global user.name "usuario_test"
RUN git config --global user.token ${GIT_TOKEN}

# Etapa final
FROM ubuntu:latest
RUN apt-get update && apt-get install -y git

COPY --from=builder /root/.gitconfig /root/.gitconfig
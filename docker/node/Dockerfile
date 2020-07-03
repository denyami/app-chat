FROM node

ENV NODE_ENV=development

RUN npm install -g express-generator

ARG DOCKER_UID=2000
ARG DOCKER_USER=docker
ARG DOCKER_PASSWORD=docker
RUN useradd -m --uid ${DOCKER_UID} --groups sudo ${DOCKER_USER} \
  && echo ${DOCKER_USER}:${DOCKER_PASSWORD} | chpasswd
USER ${DOCKER_USER}

WORKDIR usr/src/app

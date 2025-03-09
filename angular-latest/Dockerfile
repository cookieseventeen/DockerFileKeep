# 定義可在建立映像時指定的環境變數
ARG NODE_VERSION=current-alpine
FROM node:${NODE_VERSION}

ARG ANGULAR_CLI_VERSION=latest

# 使用apk安裝git Mac M2核心版本
RUN apk add --no-cache git
#RUN apt-get update && \
#  apt-get install -y git

RUN chown -R node:node /usr/local/lib/node_modules \
  && chown -R node:node /usr/local/bin

RUN echo "Angular CLI Version:${ANGULAR_CLI_VERSION}" 

USER node
RUN npm install -g @angular/cli@${ANGULAR_CLI_VERSION}
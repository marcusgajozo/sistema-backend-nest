ARG BUILD_ENV=local

FROM node:20 as base
RUN mkdir -p /nest
RUN chown node:node /nest
WORKDIR /nest

FROM base as local
USER node
RUN npm i
CMD ["npm","run","start:dev"]

FROM ${BUILD_ENV}
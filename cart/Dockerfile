FROM node:18.20.4-alpine3.19

EXPOSE 8080

RUN addgroup -S mechanoidstore && adduser -S mechanoidstore -G mechanoidstore

WORKDIR /opt/server

ENV MONGO=true

RUN chown -R mechanoidstore:mechanoidstore /opt/server

USER mechanoidstore

COPY package.json /opt/server

COPY server.js /opt/server

RUN npm install

RUN echo Hello World

CMD ["node", "server.js"]
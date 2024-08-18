FROM node:18.20.4-alpine3.19

EXPOSE 8080

RUN addgroup -S mechanoidstore && adduser -S mechanoidstore -G mechanoidstore

WORKDIR /opt/server

ENV MONGO=true

USER mechanoidstore

RUN chown -R mechanoidstore:mechanoidstore /opt/server

COPY package.json /opt/server

COPY server.js /opt/server

RUN npm install

CMD ["node", "server.js"]
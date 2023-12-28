FROM node:latest
EXPOSE 8080
RUN addgroup -S cart && adduser -S -G cart cart
WORKDIR /opt/server
RUN chown -R cart:cart /opt/server
USER cart
COPY package.json .
COPY server.js .
RUN npm install
CMD ["node", "server.js"]
FROM node:latest
EXPOSE 8080
RUN groupadd -r cart && useradd -r -g cart cart
WORKDIR /opt/server
RUN chown -R cart:cart /opt/server
USER cart
COPY package.json .
COPY server.js .
RUN npm install
CMD ["node", "server.js"]
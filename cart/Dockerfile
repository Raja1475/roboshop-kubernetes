FROM node:latest
EXPOSE 8080
RUN groupadd -r cart && useradd -r -g cart cart
WORKDIR /opt/server
RUN chown -R cart:cart /opt/server
USER cart
COPY package.json .
COPY server.js .
RUN mkdir -p /home/cart/.npm && chown -R cart:cart /home/cart
RUN npm install
CMD ["node", "server.js"]
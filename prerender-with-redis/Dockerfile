FROM node:alpine
RUN mkdir /data && cd /data \
&& git clone git@github.com:sdandroid/prerender.git \
&& cd prerender \
&& npm install

WORKDIR /data/prerender

EXPOSE 3000

CMD [ "npm", "server.js" ]
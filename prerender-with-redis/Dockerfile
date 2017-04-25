FROM node
RUN mkdir /data && cd /data \
&& git clone https://github.com/sdandroid/prerender.git \
&& cd prerender \
&& npm install

WORKDIR /data/prerender

EXPOSE 3000

CMD [ "npm", "server.js" ]

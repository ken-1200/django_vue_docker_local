FROM node:lts-alpine

WORKDIR /app

RUN apk update && \
    yarn global add @vue/cli@3.12.0 && \
    npm install vue-router && \
    npm install -y vuex && \
    npm install axios --save && \
    npm install vuetify --save && \
    npm install sass-loader node-sass --save-dev && \
    npm install --save-dev core-js@3 && \
    npm install moment --save && \
    npm install moment-timezone

ADD . /app

RUN npm run build

EXPOSE 8080

CMD ["npm", "run", "start"]

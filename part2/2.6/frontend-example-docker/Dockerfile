FROM node:10.15.0-jessie

WORKDIR /project

EXPOSE 5000

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

RUN set -e \
	&& npm build

ENV BACKEND_URL=http://localhost:8000

CMD npm start

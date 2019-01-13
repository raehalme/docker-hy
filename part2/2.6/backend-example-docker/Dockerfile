FROM node:10.15.0-jessie

WORKDIR /project

EXPOSE 8000

RUN set -e \
	&& npm install -g serve

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

ENV FRONT_URL=http://localhost:5000

CMD npm start

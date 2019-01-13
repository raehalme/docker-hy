FROM node:10.15.0-jessie

WORKDIR /project

EXPOSE 8000

RUN set -e \
	&& npm install -g serve

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

CMD FRONT_URL=http://localhost:5000 npm start

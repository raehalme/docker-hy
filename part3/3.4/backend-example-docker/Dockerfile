FROM node:10.15.0-alpine

RUN set -e \
		&& addgroup -S app \
		&& adduser -S -h /project -G app app

USER app

WORKDIR /project

EXPOSE 8000

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

ENV FRONT_URL=http://localhost:5000

CMD npm start

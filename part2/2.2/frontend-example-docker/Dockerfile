FROM node:10.15.0-jessie

WORKDIR /project

EXPOSE 5000

RUN set -e \
	&& npm install -g serve

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

RUN set -e \
	&& API_URL=http://localhost:8000 npm run build

CMD serve -s -l 5000 dist

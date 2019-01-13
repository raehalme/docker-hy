FROM ubuntu:16.04

RUN set -e \
	&& apt-get -q update \
	&& apt-get install -yq curl \
	&& curl -sL https://deb.nodesource.com/setup_10.x | bash \
	&& apt-get install -yq nodejs \
	&& apt-get purge -y --auto-remove curl \
	&& rm -rf /var/lib/apt/lists/*

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

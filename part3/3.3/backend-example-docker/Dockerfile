FROM ubuntu:16.04

RUN set -e \
	&& apt-get -q update \
	&& apt-get install -yq curl \
	&& curl -sL https://deb.nodesource.com/setup_10.x | bash \
	&& apt-get install -yq nodejs \
	&& apt-get purge -y --auto-remove curl \
	&& rm -rf /var/lib/apt/lists/* \
	&& useradd -m app \
	&& mkdir /project \
	&& chown app:app /project
	

USER app

WORKDIR /project

EXPOSE 8000

COPY package.json /project

RUN set -e \
	&& npm install

COPY . /project

ENV FRONT_URL=http://localhost:5000

CMD npm start

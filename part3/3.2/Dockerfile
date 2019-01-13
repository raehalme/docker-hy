FROM python:3.7.2-alpine3.8

RUN set -e \
		&& apk add --no-cache gcc musl musl-dev libxml2 libxml2-dev libxslt libxslt-dev wget ffmpeg \
		&& pip3 install --user --upgrade yle-dl

RUN set -e \
		&& apk del gcc musl-dev libxml2-dev libxslt-dev \
		&& rm -rf /root/.cache

WORKDIR /videos

VOLUME /videos

ENTRYPOINT [ "/root/.local/bin/yle-dl" ]

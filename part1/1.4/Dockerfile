FROM ubuntu

RUN set -e \
	&& apt-get -q update \
	&& apt-get -y install curl

ADD run.sh /

CMD /run.sh


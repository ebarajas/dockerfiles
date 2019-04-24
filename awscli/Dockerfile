FROM alpine:latest

RUN apk --no-cache add \
	ca-certificates \
	groff \
	less \
	python \
	py2-pip \
	&& pip install awscli \
	&& apk del py2-pip

ENTRYPOINT ["aws"]

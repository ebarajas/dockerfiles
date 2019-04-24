FROM python:3.7-alpine

RUN builddeps='\
		musl-dev \
		openssl-dev \
		libffi-dev \
		gcc \
		make \
		' \
	&& apk --no-cache add \
		ca-certificates \
		docker \
		git \
		py3-paramiko \
		py3-yaml \
		py3-jinja2 \
		py3-httplib2 \
		py3-pynacl \
		$builddeps \
	&& pip install --upgrade pip \
	&& pip install \
		ansible \
		awscli \
		docker \
		six \
		boto \  
		boto3 \
		botocore \
		requests \
		virtualenv \
	&& apk del --purge $builddeps  

ENTRYPOINT [ "ansible" ]

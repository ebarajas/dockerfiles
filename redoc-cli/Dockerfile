FROM node:current-alpine

RUN builddeps=' \
	ca-certificates \ 
	nghttp2-libs \
	libssh2 \
	libcurl \ 
	expat \
	pcre2 \
	git \
	' \
	&& apk add --no-cache $builddeps \
	&& npm install -g redoc-cli \
	&& apk del --purge $builddeps

ENTRYPOINT ["redoc-cli"]

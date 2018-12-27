FROM ruby:2.3-alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS build-base ca-certificates curl sqlite-dev \
    && apk add --no-cache --no-progress libstdc++ sqlite-libs \
\
    # Install dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- install \
\
    # Install mailcatcher
\
    && gem install --no-verbose mailcatcher \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS \
    && rm -f -r /root/.gem /tmp/*

ENTRYPOINT [ "dumb-entrypoint" ]

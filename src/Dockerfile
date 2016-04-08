FROM alpine:3.3

MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    MAILCATCHER_VERSION=0.6.4

RUN set -x \

    # Prepare system

    && apk add -U \

    # Install packages

    && BUILD_DEPS="build-base ruby-dev sqlite-dev" \

    && apk add \
           $BUILD_DEPS \
           libstdc++ \
           ruby \
           ruby-bigdecimal \
           sqlite-libs \

    && gem install -V --no-ri --no-rdoc \
           mailcatcher:$MAILCATCHER_VERSION \

    # Clean

    && apk del \
           $BUILD_DEPS \

    && rm -rf \
           /var/cache/apk/*

ENTRYPOINT [ "/usr/bin/mailcatcher" , "-f" ]

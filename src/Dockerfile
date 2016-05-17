FROM alpine:3.3

MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    MAILCATCHER_VERSION=0.6.4

RUN set -x \

    # Install packages

    && apk add --no-cache --no-progress --virtual build_deps \
           build-base \
           ruby-dev \
           sqlite-dev \

    && apk add --no-cache --no-progress \
           libstdc++ \
           ruby \
           ruby-bigdecimal \
           sqlite-libs \

    # Install mailcatcher

    && gem install -V --no-ri --no-rdoc \
           mailcatcher:$MAILCATCHER_VERSION \

    # Clean

    && apk del --no-progress \
           build_deps

ENTRYPOINT [ "/usr/bin/mailcatcher" , "-f" ]

FROM ruby:2.3-alpine

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    MAILCATCHER_VERSION=latest

RUN set -eux \

    # Install packages

    && apk add --no-cache --no-progress --virtual BUILD_DEPS \
           build-base \
           ca-certificates \
           curl \
           sqlite-dev \

    && apk add --no-cache --no-progress \
           libstdc++ \
           sqlite-libs \

    # Install dumb-entrypoint

    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Install mailcatcher

    && export $(curl "https://raw.githubusercontent.com/timonier/version-lister/release/generated/mailcatcher/${MAILCATCHER_VERSION}" | xargs) \

    && gem install --no-rdoc --no-ri --no-verbose \
           "mailcatcher:${MAILCATCHER_VERSION}" \

    # Clean

    && apk del --no-progress \
           BUILD_DEPS

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]

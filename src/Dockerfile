FROM alpine:3.4

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    MAILCATCHER_VERSION=0.6.4

RUN set -x \

    # Install packages

    && apk add --no-cache --no-progress --virtual build_deps \
           build-base \
           ca-certificates \
           curl \
           ruby-dev \
           sqlite-dev \

    && apk add --no-cache --no-progress \
           libstdc++ \
           ruby \
           ruby-bigdecimal \
           sqlite-libs \

    # Install mailcatcher

    && gem install -V --no-ri --no-rdoc \
           mailcatcher:${MAILCATCHER_VERSION} \

    # Install timonier/dumb-entrypoint

    && curl -sL "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Clean

    && apk del --no-progress \
           build_deps

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" , "mailcatcher" , "-f" ]

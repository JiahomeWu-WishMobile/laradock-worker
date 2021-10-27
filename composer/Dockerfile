FROM laradock-worker/php-worker

RUN set -eux ; \
  apk add --no-cache --virtual .composer-rundeps \
    p7zip \
    bash \
    coreutils \
    git \
    make \
    mercurial \
    openssh-client \
    patch \
    subversion \
    tini \
    unzip \
    zip
    
COPY installComposer.sh installComposer.sh 
RUN sh installComposer.sh
COPY docker-entrypoint.sh /docker-entrypoint.sh
RUN chown ${PUID}:${PGID} /docker-entrypoint.sh
RUN chmod 777 /docker-entrypoint.sh
WORKDIR /app

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["composer"]
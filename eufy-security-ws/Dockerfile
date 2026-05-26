ARG BUILD_FROM
FROM $BUILD_FROM

WORKDIR /usr/src/app
RUN \
    set -x \
    && apk add --no-cache \
        nodejs \
        npm \
        jq \
        git \
    && npm install --force \
    "github:Vestium-R/eufy-security-ws"

COPY run.sh /
RUN chmod a+x /run.sh
WORKDIR /data

CMD [ "/run.sh" ]
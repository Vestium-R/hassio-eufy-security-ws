ARG BUILD_FROM
FROM $BUILD_FROM

WORKDIR /usr/src/app
RUN apk add --no-cache nodejs jq
COPY node_modules ./node_modules/
COPY run.sh /
RUN chmod a+x /run.sh
WORKDIR /data

CMD [ "/run.sh" ]

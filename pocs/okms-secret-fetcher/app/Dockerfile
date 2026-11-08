FROM docker.io/library/alpine@sha256:f59abe656b692d901e184be3445e084786602108599d2a51d229c0f5a48c71bf

RUN apk add --no-cache bash curl openssl jq ca-certificates

COPY kms-get-secret.sh /usr/local/bin/kms-get-secret.sh
RUN chmod +x /usr/local/bin/kms-get-secret.sh

RUN adduser -D -u 10001 app
USER 10001

ENTRYPOINT ["/usr/local/bin/kms-get-secret.sh"]

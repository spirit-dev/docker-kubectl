ARG alpine_version

FROM gitlab-registry-internal.spirit-dev.net/infrastructure/docker/alpine:${alpine_version}

ARG alpine_version git_hash \
    build_date \
    architecture

LABEL alpine_version="${alpine_version}" \
    spiritdev_official="yes" \
    layer="1" \
    from="gitlab-registry-internal.spirit-dev.net/infrastructure/docker/alpine:${alpine_version}" \
    maintainer="bordat.jean@gmail.com"

RUN apk add --no-cache kubectl --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community

CMD ["/usr/bin/kubectl"]

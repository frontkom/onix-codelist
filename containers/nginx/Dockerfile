ARG BASE_TAG=1
FROM wodby/nginx:${BASE_TAG}

ENV NGINX_VHOST_PRESET=php

COPY --chown=wodby:wodby . .

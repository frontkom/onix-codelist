ARG BASE_TAG=7.4
FROM wodby/php:${BASE_TAG}

COPY --chown=wodby:wodby . .

RUN set -euo pipefail ; \
  composer self-update --1 ; \
  composer install --no-dev --no-interaction --no-progress --no-suggest --optimize-autoloader

USER root
RUN set -euo pipefail ; \
  ls -l /var/www/html ; \
  chown -R www-data:www-data /var/www/html/storage  /var/www/html/bootstrap/cache ;
USER wodby

ARG container_VER=0.3.0
# Fetch image https://github.com/mem76/skodaLnxCmd/blob/master/Dockerfile
FROM ghcr.io/mem76/skodalnxcmd:$container_VER
COPY sample.skoda.yaml /var/www/
COPY ha_server.php /var/www/
# Force Docker cache prune on alpine repo change.
ADD "https://dl-cdn.alpinelinux.org/alpine/last-updated" /tmp/alpine_last_updated
RUN apk --no-cache upgrade && rm /tmp/alpine_last_updated
# Instruct script to run in headless mode (no user input for pin)
ENV SKODA_HEADLESS=1
CMD ["php", "-S", "0.0.0.0:8080", "/var/www/ha_server.php"]

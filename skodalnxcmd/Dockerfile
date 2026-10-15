ARG container_VER=0.2.0
FROM ghcr.io/mem76/skodalnxcmd:$container_VER
COPY sample.skoda.yaml /var/www/
COPY ha_server.php /var/www/
RUN apk --no-cache upgrade
# Instruct script to run in headless mode (no user input for pin)
ENV SKODA_HEADLESS=1
CMD ["php", "-S", "0.0.0.0:8080", "/var/www/ha_server.php"]
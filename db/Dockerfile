FROM mysql:8.0

LABEL org.opencontainers.image.author="hamza" \
      org.opencontainers.image.description="mysql database" \
      org.opencontainers.image.version="1.0"

ENV MYSQL_NAME=appdb \
    MYSQL_ROOT_PASSWORD=root \
    MYSQL_PORT=3306

COPY init.sql /docker-entrypoint-initdb.d/

EXPOSE 3306

HEALTHCHECK --interval=10s --timeout=5s --start-period=30s --retries=5 \
  CMD mysqladmin ping -h localhost -u root -p${MYSQL_ROOT_PASSWORD} || exit 1


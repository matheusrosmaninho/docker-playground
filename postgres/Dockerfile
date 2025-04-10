ARG POSTGRES_VERSION

FROM postgres:${POSTGRES_VERSION}

# Configura idioma
RUN localedef -i pt_BR -c -f UTF-8 -A /usr/share/locale/locale.alias pt_BR.UTF-8
ENV LANG pt_BR.utf8

COPY ./scripts/postgres.sh /docker-entrypoint-initdb.d/postgres.sh
RUN chmod +x /docker-entrypoint-initdb.d/postgres.sh

EXPOSE 5432
CMD [ "postgres" ]
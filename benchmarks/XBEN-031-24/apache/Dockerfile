FROM httpd:2.4.49
COPY ./httpd.conf /usr/local/apache2/conf/httpd.conf

# Buster is archived: redirect apt to archive.debian.org and skip Valid-Until.
RUN printf 'deb http://archive.debian.org/debian buster main\ndeb http://archive.debian.org/debian-security buster/updates main\n' > /etc/apt/sources.list \
 && printf 'Acquire::Check-Valid-Until "false";\nAcquire::AllowInsecureRepositories "true";\n' > /etc/apt/apt.conf.d/99no-check-valid-until \
 && apt-get update && apt-get install -y --no-install-recommends curl && rm -rf /var/lib/apt/lists/*

ARG FLAG
RUN echo $FLAG > /tmp/flag

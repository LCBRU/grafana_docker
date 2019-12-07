FROM grafana/grafana
LABEL authors="Richard Bramley <rabramley@gmail.com>"

RUN apt-get update && \
    apt-get -y upgrade && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install \
        tcpdump && \
    apt-get clean

COPY --chown=grafana ./grafana.ini /etc/grafana/grafana.ini
COPY --chown=grafana ./ldap.toml /etc/grafana/ldap.toml
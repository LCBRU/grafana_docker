FROM grafana/grafana
LABEL authors="Richard Bramley <rabramley@gmail.com>"

COPY --chown=grafana ./grafana.ini /etc/grafana/grafana.ini
COPY --chown=grafana ./ldap.toml /etc/grafana/ldap.toml
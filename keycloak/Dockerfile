# Keyclaok version: 26.1.2
FROM quay.io/keycloak/keycloak:26.1.2

# Copy BouncyCastle FIPS providers
COPY BCFIPS/* /opt/keycloak/providers/

ENTRYPOINT ["/opt/keycloak/bin/kc.sh"]

EXPOSE 8080
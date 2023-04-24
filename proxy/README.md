# Traefik Reverse Proxy Example

This example sets up a [Traefik](https://docs.traefik.io) reverse proxy for other projects to share use of.

## Usage

```bash
# Bring up the compose stack from this `proxy` folder.
docker compose up -d
```

## Adding HTTPS support

If you want to enable HTTPS support, you can add a certificate and private key to the `traefik` sub-folder (the `.crt` is there if you want to look at its SAN with `openssl x509 -in traefik/localtest.me.crt -noout -text`).  Then, simply rename `docker-compose.override.example.yml` to `docker-compose.override.yml` and re-up the stack.  The [override YAML](https://docs.docker.com/compose/extends/#understanding-multiple-compose-files) adds the additional features to the Reverse Proxy to enable TLS termination and automatic redirects.

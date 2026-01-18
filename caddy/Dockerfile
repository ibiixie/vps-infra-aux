FROM caddy:2.10-builder AS builder
RUN xcaddy build v2.10 --with github.com/mholt/caddy-l4

FROM caddy:2.10-alpine
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
COPY ./Caddyfile /etc/caddy/Caddyfile

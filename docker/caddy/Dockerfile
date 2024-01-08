# Build a custom caddy image with cloudflare plugins
FROM caddy:builder-alpine AS builder

RUN xcaddy build \
    --with github.com/WeidiDeng/caddy-cloudflare-ip \
    --with github.com/caddy-dns/cloudflare

FROM caddy:aline

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
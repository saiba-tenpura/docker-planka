# Planka Compose
My personal Planka docker compose setup incl. an external Traefik instance for serving the web interface.

## Traefik Reverse Proxy
For as how to setup the Traefik refer to this [repository](https://github.com/saiba-tenpura/traefik-proxy).

## Setup
Copy the .env.example file, set the passwords and adjust the variables to match your environment.
```bash
cp .env.example .env

# Generate a secret key / Postgres password
openssl rand -hex 64
```

Create an admin user.
```bash
docker compose run --rm planka npm run db:create-admin-user
```

For additional information refer to the [official documentation](https://docs.planka.cloud).

## License
[MIT](./LICENSE)

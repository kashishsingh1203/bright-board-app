# Brightboard

Laravel 9 API starter with PHP 8.2, Nginx, MySQL, and Redis. The local Docker
environment includes a Redis queue worker and initializes the app key and
database on first start.

## Run locally

Requires Docker Engine and the Docker Compose plugin.

```sh
docker compose up --build
```

Open [http://localhost:8080](http://localhost:8080) to see Laravel's welcome
page. Stop the services with `Ctrl+C`.

The Compose file uses development-only database credentials. Do not reuse them
outside local development.

## Laravel version note

This project intentionally uses Laravel 9 as requested. Laravel 9 is no longer
security-supported. Composer reports seven advisories for `laravel/framework`,
including a critical authentication-bypass advisory (CVE-2026-114509).
Composer is configured not to block dependency installation so the requested
stack can build; the advisories are still reported. Do not expose this starter
outside local development or use it with customer data. Upgrade to a supported
Laravel release before adding authentication or account-scoped data.
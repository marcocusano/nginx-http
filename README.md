# nginx-http

NGINX is a high-performance HTTP server and reverse proxy, as well as an IMAP/POP3 proxy server. It is known for its stability, rich feature set, simple configuration, and low resource consumption.

For more information, visit the [official NGINX website](https://nginx.org/) and the [NGINX documentation](https://nginx.org/en/docs/).

## Configuration Files Description

This folder contains various configuration files for NGINX, useful as templates for managing HTTP configuration.

### proxy.conf
Configures proxy headers to forward client information to the backend server. Example:
- Sets headers like `Host`, `X-Real-IP`, `X-Forwarded-For`, and `X-Forwarded-Proto`.

### proxy.upgrade.conf
Configures the proxy to handle WebSocket connections. Example:
- Upgrades HTTP connections to WebSocket using headers like `Upgrade` and `Connection`.

### redirect.conf
Configures a redirect to a specific domain. Example:
- Redirects all traffic to `https://www.marcocusano.dev`.

### redirect.default.conf
Configures a default redirect to HTTPS. Example:
- Redirects all HTTP traffic to HTTPS using the same host.

### root.default.conf
Sets the default server root directory and index files. Example:
- Defines the root directory as `/var/www/html` and sets default index files like `index.php` and `index.html`.

### services
Configuration files for various services.
- phpMyAdmin
- pgAdmin

### whitelist.conf
Configures allowed and denied access based on IP addresses. Example:
- Allows access from a specific IP address and denies all other traffic.

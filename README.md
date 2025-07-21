# Nginx Virtual Host Setup Script

This script automates the creation of a secure Nginx virtual host (with optional WordPress installation), including:

- SSL-ready Nginx configuration (self-signed or predefined)
- PHP-FPM socket detection and integration
- Directory creation for public files and logs
- Optional WordPress installation
- Automatic MySQL database creation
- `/etc/hosts` update for local development

---

## ✅ Features

- Validates domain and PHP-FPM version input
- Configures **HTTPS** virtual host with **HSTS**
- Adds optional `uploads` subdomain
- Supports PHP-FPM 5.6, 7.x, 8.x
- Creates MySQL database (UTF8MB4)
- Optional WordPress auto-setup
- Adds entries to `/etc/hosts`
- Safe prompts to avoid overwrites

---

## ⚙️ Requirements

Ensure the following are installed before running:

- Nginx
- PHP-FPM (e.g., `php8.3-fpm`)
- `unzip`
- `wget`
- MySQL/MariaDB client (`mysql`)
- Nginx snippets:
  - `/etc/nginx/snippets/self-signed.conf`
  - `/etc/nginx/snippets/ssl-params.conf`
  - `/etc/nginx/snippets/fastcgi-php.conf`

---

## 🚀 How to Use

> **Run as root or using `sudo`:**

```bash
sudo bash nginx-virtual-host.sh

# Bitwarden_rs Docker Compose

This micro-repo is used only as a host for an easily hostable Bitwarden_rs config

## Setup

To setup this repo for deployment, clone it onto your docker server and enter the required values into the .env file.

VIRTUAL_HOST and LETSENCRYPT_HOST should be the same values, your website domain name. Ex: `passwords.example.com`

The DEFAULT_EMAIL env will allow letsencrypt to email you if your certificates are going to expire soon

Running `docker-compose up -d` should be all that is required to host your own instance of Bitwarden_rs.

## Gotchas

Due to the nginx proxy binding itself on ports 80 and 443, you cannot have another web server like Apache or Nginx running on the local machine.

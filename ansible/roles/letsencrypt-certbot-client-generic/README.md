# Letsencrypt (Certbot) client

This is the role for any server that uses the Certbot client
of Letsencrypt service.

Requires the following variables preconfigured:

- `letsencrypt_domains` – the list of the domains for which to request the SSL
    certificate. The first one must be the most-top-level, e.g.
    `letsencrypt_domains: [myserver.com www.myserver.com]`
- `letsencrypt_webroot` – the directory where the Certbot will store
    the Letsencrypt handshake files. In this directory, the `.well-known`
    will be created; your web server must be prepared to serve the files from
    `{{ letsencrypt_webroot }}/.well-known` directory under the `/.well-known/`
    URL.
- `letsencrypt_email` – the contact email to be reported to Letsencrypt.
- `restart_web_server_handler` – the Ansible handler which should be called
    to restart the Web server after the Letsencrypt handshake directory
    is prepared.

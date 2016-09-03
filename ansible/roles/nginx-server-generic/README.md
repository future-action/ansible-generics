# Nginx server

This is the role for any server that uses the Nginx server for static files serving.

Requires the following variables preconfigured:

- `nginx_site_conf_template_dir` – from what local directory Ansible should take
  the templates of the site confs.  This template can use variables:
  + `nginx_ssl_is_enabled` - configured depending on the variables
    `nginx_ssl_certificate_path` and `nginx_ssl_certificate_key_path` (see below).
    Note that if you are getting the SSL certificate using Letsencrypt,
    it may be not available yet by the moment of configuration, but will be
    available by its end; so, it is required to run Ansible twice.

- `nginx_sites_available` – the list of the Nginx sites to consider available.
- `nginx_sites_enabled` – the list of the Nginx sites to consider available.
- `nginx_ssl_certificate_path` – the path to the SSL certificate; see the comment
  to the next variable.
- `nginx_ssl_certificate_key_path` – the path to the SSL certificate key; if
  any of `nginx_ssl_certificate_path` or `nginx_ssl_certificate_key_path` files
  are missing, SSL is assumed disabled.

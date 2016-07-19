# Nginx server

This is the role for any server that uses the Nginx server for static files serving.

Requires the following variables preconfigured:

- `nginx_site_conf_template_dir` – from what local directory Ansible should take
  the templates of the site confs. 
- `nginx_sites_available` – the list of the Nginx sites to consider available.
- `nginx_sites_enabled` – the list of the Nginx sites to consider available.

# Gunicorn server

This is the role for any server that uses the Gunicorn server.

Requires the following variables preconfigured:

- `gunicorn_site_conf_template_dir` – from what local directory
  should Ansible take the templates of the site confs. 
- `gunicorn_sites_available` - the list of the sites which may be present (but not necessarily enabled).
- `gunicorn_sites_enabled` – the list of the sites to be applied and enabled.

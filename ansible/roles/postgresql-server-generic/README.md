# postgresql-server-generic

This is the role for any server that runs the PostgreSQL database.

Requires the following variables preconfigured:

- `postgresql_server_db_settings` – should contain the list of per-DB settings.
  Each per-DB setting set is a dictionary with `db` and `owner` keys.

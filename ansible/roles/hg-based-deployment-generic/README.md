# hg-based deployment

This is the role for any server that uses the HG (Mercurial)-based deployment of the project.

Requires the following variables preconfigured:

- `hg_project_username` – what username should Mercurial use to clone the repository.
  Example: `project_username`
- `hg_repository_url` – what repository to clone.
  Example: `myproject_repository_url`
- `hg_repository_host` – the host part of the `hg_repository_url`.
  Example: `bitbucket.org`
- `hg_clone_path` – where to clone the repository.
  Example: `{{ project_home }}/subdir`
- `hg_clone_branch` – what branch to clone.
  Example: `{{ myproject_branch }}`
- `hg_update_handler` – the Ansible list of handlers which should be called if
  the code was updated from repository.
  Example: `[restart gunicorn, restart nginx]`

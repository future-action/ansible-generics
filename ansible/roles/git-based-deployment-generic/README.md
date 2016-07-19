# git-based deployment

This is the role for any server that uses the Git-based deployment of the project.

Requires the following variables preconfigured:

- `git_project_username` – what username should Git use to clone the repository.
  Example: `project_username`
- `git_repository_url` – what repository to clone.
  Example: `myproject_repository_url`
- `git_repository_host` – the host part of the `git_repository_url`.
  Example: `github.com`
- `git_clone_path` – where to clone the repository.
  Example: `{{ project_home }}/subdir`
- `git_clone_branch` – what branch to clone.
  Example: `{{ myproject_branch }}`
- `git_update_handler` – the Ansible list of handlers which should be called if
  the code was updated from repository.
  Example: `[restart gunicorn, restart nginx]`

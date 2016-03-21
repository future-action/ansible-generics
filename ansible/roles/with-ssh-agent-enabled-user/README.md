# with-ssh-agent-enabled-user

This is the role for any server that uses some non-root user for other tasks,
and this user has access to the SSH agent information of the connection.

Requires the following variables preconfigured:

- `ssh_agent_enabled_user` – what user should be allowed to get access
  to SSH agent of the connection.
  Example: `project_username`

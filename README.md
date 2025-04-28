# Ansible Roles

Ansible roles.

## Development

> First, install **python3.10** (or higher) and **docker**.

To setup your development environments, run the commands below.

```bash
# Ubuntu/Debian
sudo apt update && sudo apt install -y pipx
# RedHat
sudo dnf install -y pipx

# Python packages
pipx install --include-deps ansible-dev-tools
pipx inject --include-apps --include-deps ansible-dev-tools \
  argcomplete \
  'docker>=7.1.0' \
  'molecule<25.2.0' \
  'molecule-plugins[docker]==23.5.0' \
  'requests==2.31.0'

pipx ensurepath
source ~/.bashrc
activate-global-python-argcomplete --user

adt --version
molecule --version
```

# Jellyfin (Ansible)

[![Ansible Lint](https://github.com/leberkaslabs/ansible-jellyfin-deployment/actions/workflows/ansible-lint-action.yml/badge.svg)](https://github.com/leberkaslabs/ansible-jellyfin-deployment/actions/workflows/ansible-lint-action.yml)

This repository provides a fully automated Ansible setup for deploying Jellyfin in Docker. Optionally, an NGINX reverse proxy can be installed to secure the Jellyfin container with TLS.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- Ensure Docker is installed (you may want to checkout my [ansible-docker-role](https://github.com/DudeCalledBro/ansible-role-docker))

## Usage

Before running the playbooks, prepare the inventory and configuration files.

1. Copy the example inventory file to `hosts.yml`:

    ```bash
    cp inventories/hosts.example.yml inventories/hosts.yml
    ```

2. Run the Ansible playbooks:

    ```bash
    # Setup Jellyfin
    ansible-playbook jellyfin.yml -i inventories/hosts.yml

    # Setup Nginx
    ansible-playbook nginx.yml -i inventories/hosts.yml
    ```

## License

Copyright © 2025 Niclas Spreng

Licensed under the [MIT license](LICENSE).

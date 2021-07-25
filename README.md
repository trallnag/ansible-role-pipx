[![role](https://img.shields.io/ansible/role/55573)](https://galaxy.ansible.com/trallnag/pipx)
[![quality](https://img.shields.io/ansible/quality/55573)](https://galaxy.ansible.com/trallnag/pipx)
[![downloads](https://img.shields.io/ansible/role/d/55573?label=downloads)](https://galaxy.ansible.com/trallnag/pipx)

# Ansible Role for Pipx

Ansible role that installs [Pipx][pipx] on Linux.

[pipx]: https://github.com/pypa/pipx

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/pipx).

## Content

* Python executable can be configured.
* Installs tab completion for Bash.

## Role Variables

```yaml
pipx_version:
  default: 0.16.3
  type: raw
  required: false
  description: >-
    Pipx version to install.

pipx_default_python:
  default: python
  type: raw
  required: false
  description: >-
    Overrides default python used for commands.
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.poetry
      vars:
        pipx_version: 0.16.3
        pipx_default_python: python
```

## Special Requirements

None.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag

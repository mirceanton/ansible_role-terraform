Ansible Role: Terraform
=======================

An Ansible role that installs Terraform by downloading the precompiled binary.

Requirements
------------

N/A

Role Variables
--------------

|         Variable         |  Type  | Default |                 Description                  |
| :----------------------: | :----: | :-----: | :------------------------------------------: |
|   `terraform_version`    | string | `1.3.3` |     The version of terraform to install.     |
| `terraform_architecture` | string | `amd64` | The architecture for the binary to download. |
|      `terraform_os`      | string | `linux` |      The OS for the binary to download.      |

Dependencies
------------

N/A

Example Playbook
----------------

``` yml
---
- hosts: all
  remote_user: root

  roles:
    - role: mirceanton.terraform
      vars:
        terraform_version: "1.3.3"
        terraform_architecture: arm64
        terraform_os: linux
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).

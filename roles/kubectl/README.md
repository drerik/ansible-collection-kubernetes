drerik.kubernetes.kubectl
=========

A ansible role to dowload and install kubectl.

Requirements
------------

None

Role Variables
--------------

- `arch_type`: (Default: autodetected ) Which architecture the binary show be in.
- `kubectl_version` (Default: pulls latest version from variable `kubectl_release_number_url`)
- `kubectl_release_number_url` (Default: 'https://dl.k8s.io/release/stable.txt' ) Url to pull latest release version number from.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - drerik.kubernetes.kubectl

License
-------

Apache-2.0

Author Information
------------------

Erik Kaareng-Sunde <erik@eriksunde.com>

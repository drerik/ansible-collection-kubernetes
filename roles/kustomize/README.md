drerik.kubernetes.kustomize
=========

Installs the kustomize tool.

Requirements
------------

None

Role Variables
--------------

release_version: ( Default is pulled from github api )
release_platform: ( Default: "{{ ansible_system | lower }}" )
release_architecture: ( Default: 'amd64' )

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Install latest version on a standard x86_64 server
      hosts: servers
      roles:
        - drerik.kubernetes.kustomize

    - name: Install latest version on a standard arm64 server
      hosts: servers
      roles:
        - role: drerik.kubernetes.kustomize
          release_platform: arm64

        

License
-------

Apache-2.0

Author Information
------------------

Erik Kaareng-Sunde <erik@eriksunde.com>

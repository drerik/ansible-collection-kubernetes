drerik.kubernetes.helm
=========

Installs the helm binary

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

- `helm_release_platform`: ( Default: "{{ ansible_system | lower }}" ) Which platform the system is on ( Linux/Windows etc. )
- `helm_release_architecture`: ( Default: "amd64" ) Which architecture the system is using.
- `helm_github_release_api_url`: ( Default: "https://api.github.com/repos/helm/helm/releases" ) The url for the release api
- `helm_download_url`: ( Default: "https://get.helm.sh/helm-{{ helm_release_version }}-{{ helm_release_platform }}-{{ helm_release_architecture }}.tar.gz" ) Download url for archive.
- `helm_runtime_binary`: ( Default: "helm" ) Name of the helm binary
- `helm_runtime_install_path`: ( Default: "/usr/local/bin/" ) Where the binary should be installed to.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - drerik.kubernetes.helm

License
-------

Apache-2.0

Author Information
------------------

Erik Kaareng-Sunde

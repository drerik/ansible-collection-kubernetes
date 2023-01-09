drerik.kubernetes.k3s
=========

Installs a kubernetes instance based on k3s on a server. For more information on k3s, go to <https://k3s.io>.

Requirements
------------

No other requirements other than standard libraries.

Role Variables
--------------

- `state`: If defined and set to 'absent' will remove the k3s instance on the server.
- `k3s_channel`: ( Default: `stable` ) Specifies which version channel of k3s you want to install.
- `k3s_version`: ( Default: Gets latest version from the selected channel in `k3s_channel` ) Set this to a spesific version of k3s to pin it.

- `k3s_config`: If you define a yaml config here, it will be automatic saved to `k3s_config_file`. For more information about using config file, head to <https://rancher.com/docs/k3s/latest/en/installation/install-options/#configuration-file>
- `k3s_config_file`: ( Default: "/etc/rancher/k3s/config.yaml" ) Specifies where to save the content of `k3s_config`.

- `k3s_cmd`: ( Default: "{{ k3s_binary }} server" ) The command the systemd service uses to run k3s.
- `k3s_binary`: ( Default: "/usr/local/bin/k3s" )  Where and what the k3s binary should be placed.

- `k3s_github_url`: ( Default: https://github.com/k3s-io/k3s/releases ) Where the ansible role should get the release list from.

- `k3s_release_channel_url`: ( Default: https://update.k3s.io/v1-release/channels ) Where the ansible role should get it's channel list from.
- `k3s_storage_url`: ( Default: https://storage.googleapis.com/k3s-ci-builds ) Where the ansible role should get the k3s binaries from.


Dependencies
------------

None

Example Playbook
----------------

Simple example:

```yaml
- name: Deploy k3s
  hosts: server
  roles:
    - drerik.kubernetes.k3s
```

For example with a simple webpage/startpage deployed, see the playbook `k3s_example` in this collection.

You can uninstall k3s by setting the state to `absent`.
```bash
ansible yourserver -m ansible.builtin.import_role -a 'name=drerik.kubernetes.k3s' -e 'state=absent'
```


License
-------

Apache 2.0

Author Information
------------------

Erik Kaareng-Sunde

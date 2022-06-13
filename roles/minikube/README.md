drerik.kubernetes.minikube
=========

Installs and configures a minikube kubernentes cluster

Requirements
------------

None

Role Variables
--------------

minikube_user: ( Default: 'minikube' )
minikube_driver: ( Default: 'docker' )

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Install latest version of minikube and starts a cluster with the docker driver
      hosts: servers
      roles:
        - drerik.kubernetes.minikube

    - name: Install latest version of minikube and starts a cluster with the local driver and as the user 'kubernetes'
      hosts: servers
      roles:
        - role: drerik.kubernetes.kustomize
          minikube_driver: local
          minikube_user: kubernetes

        

License
-------

Apache-2.0

Author Information
------------------

Erik Kaareng-Sunde <erik@eriksunde.com>

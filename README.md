Gitea
=========

This role deploys gitea in a Podman pod with an nginx reverse proxy (80 -> 3000) and a postgres backend
https://gitea.io/en-us/

Requirements
------------

This requires the containers.podman collection: https://galaxy.ansible.com/containers/podman

Role Variables
--------------

Variable              | Description
----------------------|------------------------------------------------------------------------
gitea_pod_network     | Podman network to apply to pod. (Default: 'podman')
gitea_pod_ip          | Set a static IP for the pod's shared network. (Default: '10.88.0.100')
gitea_pod_hostname    | Hostname for pod. (Default: 'gitea.example.com)
gitea_version         | Gitea version. (Default: '1.12.3')
postgres_version      | Postgres version. (Default: '9.6')
postgres_data_dir     | Data directory for Postgres container. (Default: '/var/lib/containers/gitea-postgres') 
nginx_version:        | Nginx version. (Default: 1.19.1)

Dependencies
------------

No dependencies at this time.

Example Playbook
----------------

```
    - hosts: podman-host
      roles:
         - gitea
```

License
-------

BSD

Author Information
------------------

David Chatterton
david@davidchatterton.com

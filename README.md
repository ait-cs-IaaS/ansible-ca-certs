# Ansible-Role: ca-certs

Installs CA Certificates 

## Requirements

Ubuntu > 18.04

## Role Variables

```
ca_certs_dest: /usr/local/share/ca-certificates
```

```
ca_certs_user: root
```

```
ca_certs_group
```

```
ca_certs_update: /usr/sbin/update-ca-certificates
```

```
ca_certs
```

```
ca_certs_update_certifi: no
```

```
ca_certs_python_executables
```

```
ca_certs_pip_packages
```

```
ca_certs_pip_executables
```

```
ca_certs_certifi_location_command
```

## Example Playbook

```
- hosts: localhost
  roles:
    - ca-certs
  vars:
    ca_certs_certifi_location_command: import requests; print(requests.certs.where())
    ca_certs:
      - /ad/cert1.pem
      - /asd/asd/asd7/cert2.pem
```

## License

GPL-3.0

## Author Information

AIT

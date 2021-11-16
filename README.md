# Ansible-Role: ca-certs

Manage Certificate Authorities on Linux

## Requirements

Ubuntu >= 18.04
CentOS >= 7

## Role Variables

```yaml
ca_certs_dest: /usr/local/share/ca-certificates
```

```yaml
ca_certs_user: root
```

```yaml
ca_certs_group
```

```yaml
ca_certs_update: /usr/sbin/update-ca-certificates
```

```yaml
ca_certs
```

```yaml
ca_certs_update_certifi: no
```

```yaml
ca_certs_python_executables
```

```yaml
ca_certs_pip_packages
```

```yaml
ca_certs_pip_executables
```

```yaml
ca_certs_certifi_location_command
```

## Example Playbook

```yaml
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

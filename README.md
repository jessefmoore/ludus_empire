# README

This will run BC-Security Empire via a Docker image


# Ansible Role: ludus_empire ([Ludus](https://ludus.cloud))

An Ansible Role that installs ludus_empire on ubuntu22

> [!WARNING]
> This is a warning about empire is using docker for ubuntu22 in this role

## Requirements

None.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: ludus_empire_hosts
  roles:
    - jessefmoore.ludus_empire
```

## Example Ludus Range Config

```yaml
ludus:
  - vm_name: "{{ range_id }}-ubuntu-22-empire"
    hostname: "{{ range_id }}-empire"
    template: ubuntu-22.04-x64-server-template
    vlan: 10
    ip_last_octet: 11
    ram_gb: 4
    cpus: 2
    linux: true
    roles:
      - jessefmoore.ludus_empire
```

## License

[//]: # (If you change the License type, be sure to change the actual LICENSE file as well)
GPLv3

## Author Information

This role was created by [Jesse Moore](https://github.com/jessefmoore), for [Ludus](https://ludus.cloud/).

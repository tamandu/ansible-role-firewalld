# ansible-role-firewalld

This role configures firewalld rules.

## Requirements

None.

## Role Variables

#### firewalld_service
Service must be listed in /etc/services.
```
firewalld_service:
  <service name>: <enabled or disabled>
```

#### firewalld_port
Key must be in the form PORT/PROTOCOL or PORT-PORT/PROTOCOL for port ranges.
```
firewalld_port:
  <port/protocol>: <enabled or disabled>
```

## Dependencies

None.

## Example Playbook

```yml
- hosts: servers
  roles:
    - firewalld
```

*Inside `vars/main.yml`*:  
Variables must be defined by dictionary.
```yml
firewalld_service:
  dhcpv6-client: disabled
  ssh: enabled
firewalld_port:
  8080/tcp: enabled
```

## License

MIT

## Author Information

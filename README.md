# Ansible Role: Grafana

[![Build Status](https://travis-ci.com/transitiv/ansible-role-grafana.svg?branch=master)](https://travis-ci.com/transitiv/ansible-role-grafana)

This role installs Grafana from the official package repositories on systems running Debian/Ubuntu and RHEL/CentOS.

## Requirements

Root accesss is required for installing packages, so you must run it in a playbook with global root privileges or define `become: yes` when the role is included:

```yaml
- hosts: grafana_servers
  roles:
    - role: transitiv.grafana
      become: yes
```

## Dependencies

This role has no dependencies.

## Variables

```yaml
grafana_enterprise: false
```

Determines whether to install the Enterprise Edition of Grafana.

```yaml
grafana_service_state: started
```

Sets the state of the service whenever the role is invoked (refer to the `state` parameter of the service module for valid values).

```yaml
grafana_service_enabled: true
```

Defines whether Grafana is started on boot.

## License

This role is available under the terms of the MIT license.

## Author

This role was created by [Transitiv Technologes Ltd.](https://www.transitiv.co.uk).

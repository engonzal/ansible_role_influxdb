### Ansible Role: InfluxDB (in development)

Module to install InfluxDB as a non-root user.  Service managed by systemd.  

#### Role Variables
Most of the defaults should be fine, see defaults/main.yml for more.

#### Example Playbook

```
    # First part of the play, configure things as root
    - hosts: servers
      user: root
      roles:
        - { role: engonzal.ansible_role_systemd_user, tags: [ 'systemd'] }
    # Influx play, runs as a local user on the host
    - hosts: servers
      user: engonzal
      roles:
        - { role: engonzal.ansible_role_influxdb, tags: [ 'influxdb'] }
```

#### License

BSD

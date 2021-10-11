# Ansible Role: `aisbergg.chrony`

This Ansible role installs and configures Chrony, an alternative NTP implementation.

## Requirements

Requires Systemd to be used as the service manager.

## Role Variables

| Variable | Default | Comments |
|----------|---------|----------|
| `chrony_service_enabled` | `true` | Enable/Disable the Chrony service |
| `chrony_service_state` | `started` | Set the service state (Possible values: `started`, `reloaded`, `restarted`, `stopped`) |
| `chrony_service_restart_on_change` | `true` | Restart Chrony service on configuration changes. |
| `chrony_timezone` | `Europe/Berlin` | Set the timezone of the system. A list of available time zones can be found here: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones |
| `chrony_uninstall_other_ntp_services` | `true` | If true, all other NTP programs present on the system will be uninstalled |
| `chrony_config_server` | `["0.pool.ntp.org","1.pool.ntp.org","2.pool.ntp.org", "3.pool.ntp.org"]` | List of NTP servers to be used as a time source |
| `chrony_config_pool` | `[]` | List of NTP server pools |
| `chrony_config_makestep` | `1.0 3` | Step the system clock if the adjustment is larger than a threshold value |
| `chrony_config_rtcsync` | `true` | Enable kernel synchronization of the real-time clock (RTC) |
| `chrony_config_extra_options` | `{}` | A dict (key-value pairs) of extra config options. A list of available config options can be found here: https://chrony.tuxfamily.org/doc/3.5/chrony.conf.html |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  vars:
    chrony_timezone: Europe/Berlin
    chrony_config_server:
      - 0.arch.pool.ntp.org
      - 1.arch.pool.ntp.org
    chrony_config_extra_options:
      maxupdateskew: 100.0
  roles:
    - chrony
```

## License

MIT

## Author Information

Andre Lehmann (aisberg@posteo.de)

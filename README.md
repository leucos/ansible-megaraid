ansible-megaraid role
=====================

Deploys LSI-MegaRAID utilities with ansible.

This role is datadog enabled.

Ubuntu 14.04 trusty only.

# Variables

There are no megaraid variables. Only datadog ones:

- `datadog_enabled:` whether datadog is enabled (default: false)
- `datadog_base_path`: top level directory for scripts and configs (default: `/etc/dd-agent/`)
- `datadog_megaraid_adapter_events`: do we send events for adapter issues (default: 0)
- `datadog_megaraid_disk_events`: do we send events for disk issues (default: 0)

Please, check caveats [heare](https://github.com/leucos/datadog-megaraid) when setting the two last variables to 1.

# Usage

    - hosts: hosts_with_lsi_megaraid
      roles:
        - ansible-megaraid

# Notes

See [datadog-agent](https://github.com/leucos/ansible-datadog-agent) role and  [datadog-megaraid](https://github.com/leucos/datadog-megaraid) check utility.

Michel Blanc <mb@mbnet.fr>

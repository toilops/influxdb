InfluxDB
=========

Ansible role to install and configure the InfluxDB.

Requirements
------------

Running Linux system with SSD storage.

Role Variables
--------------

This role currently has the following variables that can be overridden within your playbook.

```yaml
influxdb_name: influxdb # Package name to install
influxdb_version: latest # Version of the influxDB to install.
```

Dependencies
------------

This role requires you to configure the InfluxData repositories. `toilops.influxdata_repo` will do this work for you and has been included as a role depenency.

Install the role by executing: `ansible-galaxy install toilops.influxdata_repo`

Example Playbook
----------------

Example on how to include this role into your playbook.

    - hosts: servers
      tasks:
        - name: Install InfluxDB
          include_role:
            name: toilops.influxdb
          vars:
            influxdb_version: influxdb-1.6.4

License
-------

MIT

Author Information
------------------

Find me on github [@BondAnthony](https://github.com/BondAnthony)

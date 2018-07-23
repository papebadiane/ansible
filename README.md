Ansible role: Import kibana's dashboard and visualization
=====

# Requirement

None


# Role Variables

The Variables listed below is setup with default values (see `defaults/main.yml`)

kibana's group host and interface

```
server_group: server
interface: lo
```
Path of file which content the
```
dashboard_path: ./dashboard.json
visualization_path: ./visualization.json
search_path: ./search.json
```
Kibana index pattern and time filter that will be create.
```
index_pattern: "oio-*"
time_filter: "@timestamp"

```


# Examples Playbook

```
- hosts : server
  roles:
    - role: kibana-import-dashboard-and-visualization
```

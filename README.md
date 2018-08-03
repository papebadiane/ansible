Ansible role: Import kibana's dashboard and visualization
=====

# Requirement

None


# Role variables

The Variables listed below is setup with default values (see `defaults/main.yml`)

 Group (of inventory) and interface of the kibana server

```
server_group: server
interface: lo
```
Kibana's object to import
```
kibana_import_dashboard_enabled: true
kibana_import_visualization_enabled: true
kibana_import_search_enabled: true

dashboard_path: ./dashboard.json
visualization_path: ./visualization.json
search_path: ./search.json
```
Kibana index pattern and time filter that will be create.
```
index_pattern: "oio-*"
time_filter: "@timestamp"

```

In case authentication with a user and a password is required, you will have to define the following variables 
```
kibana_user: "kibana"
kibana_password: "kibana"

```

# Examples Playbook

```
- hosts : server
  roles:
    - role: kibana-import-dashboard-and-visualization
```

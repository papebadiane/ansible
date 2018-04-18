Ansible role: Import kibana's dashboard and visualization
=====


# Role Variables 

 
```
server_group: server
interface: lo
```

```
dashboard_path: ./dashboard.json
visualization_path: ./visualization.json
```

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

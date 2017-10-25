# grafana_dashboards

example config for elasticsearch_exporter:

```
- job_name: 'elasticsearch'

  scrape_interval: 30s
  metrics_path: '/metrics'
  static_configs:
    - targets: [ 'master1']
      # Labels assigned to all metrics scraped from the targets.
      labels:
        node_type: data
    - targets: [ 'storage1' ]
      # Labels assigned to all metrics scraped from the targets.
      labels:
        node_type: master
    - targets: [ 'client1' ]
      # Labels assigned to all metrics scraped from the targets.
      labels:
        node_type: client
```

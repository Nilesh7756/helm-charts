# helm-charts
Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack with HTTP servers, databases, caches, and so on.  Charts are created as files laid out in a particular directory tree, then they can be packaged into versioned archives to be deployed.


##Structure of a Chart

```
.
├── Chart.yaml
├── README.md
├── templates
│   ├── NOTES.txt
│   ├── _helpers.tpl
│   ├── configmap.yaml
│   ├── deployment.yaml
│   ├── pvc.yaml
│   ├── secrets.yaml
│   └── svc.yaml
└── values.yaml
```

Chart.yaml = contains some metadata about the Chart, such as its name, version, keywords.
values.yaml=contains keys and values that are used to generate the release in your Cluster. These values are replaced in the resource manifests .
configMap.yaml=contains database configuration.
secrets.yaml= database passwords are stored in secret file.

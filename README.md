# Traefik Mesh

Traefik Mesh is a simple, yet full-featured service mesh. It is container-native and fits as your de-facto service mesh in your Kubernetes cluster.
It supports the latest Service Mesh Interface specification [SMI](https://smi-spec.io/) that facilitates integration with pre-existing solution.

Moreover, Traefik Mesh is opt-in by default, which means that your existing services are unaffected until you decide to add them to the mesh.

## Prerequisites

- Kubernetes 1.11+
- CoreDNS/KubeDNS installed as [Cluster DNS Provider](https://kubernetes.io/docs/tasks/administer-cluster/dns-custom-nameservers/) (versions 1.3+ supported)
- [Helm v3](https://helm.sh/docs/intro/install/)

## Installing the Chart

To install the chart with the release name `traefik-mesh`:

```bash
$ helm repo add traefik-mesh https://helm.traefik.io/mesh
$ helm repo update
$ helm install traefik-mesh traefik-mesh/traefik-mesh
```

You can use the `--namespace my-namespace` flag to deploy Traefik Mesh in a custom namespace and the `--set "key1=val1,key2=val2,..."` flag to configure it.
Where `key1=val1`, `key2=val2`, `...` are chart values that you can find in the [values.yaml](https://github.com/traefik/mesh-helm-chart/tree/master/mesh/values.yaml) file.

## Uninstalling the Chart

To uninstall the chart with the release name `traefik-mesh`:

```bash
$ helm uninstall traefik-mesh
```

## Configuration

For a detailed list of the available configuration options, check out the [configuration](https://github.com/traefik/mesh-helm-chart/tree/master/mesh#configuration) section in the chart readme.

## Contributing

If you want to contribute to this chart, please read the [Guidelines](https://github.com/traefik/mesh-helm-chart/blob/master/mesh/Guidelines.md).

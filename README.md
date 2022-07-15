# traefik-sample

In order to run Traefik at the namespace scope there are the following requirements:

- Create an ingress class: `kubectl apply -f manifests/ingress-class.yml`
- Create a cluster role with access to ingress classes: `kubectl apply -f manifests/cluster-role.yml`
- In your okteto installation, add this to your `values.yml`:

```
globalClusterRole: okteto-read-ingress-class
```

Happy coding!
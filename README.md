# harbor-project-proxy

This is a simple helm-chart for proxying mirrors from Harbor to a Ingress.
Just in case if you using non nginx-ingress solution in your cluster.

### How to use it:

The first section of the DNS name is parsed and proxies traffic to a project in the harbor with the same name.
For example:
`docker-hub-mirror.some.other.dns.name` will direct traffic to harbor project `docker-hub-mirror`.

By default this helm chart point to kubernetes service `harbor-web`, if you want to change this point you can change `harborUpstream` value.

### How to pull it:
```shell
helm pull oci://ghcr.io/hiddenmarten/harbor-project-proxy
```

### Thanks to these guys for inspiring:
- @pedroosorio
- @jgallucci32
- @ricardojdsilva87 

### For more information:
- https://github.com/goharbor/harbor/issues/8082

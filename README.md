# Rancher Helm Chart Testing

## Instructions

```sh
helm repo add rancher-latest https://releases.rancher.com/server-charts/latest
helm pull rancher-latest/rancher
tar -xf rancher-2.5.6.tgz
helm lint rancher/*
helm repo index --url https://github.com/oxr463/rancher-helm-chart-testing .
```

## Reference

- [Create a public Helm chart repository with GitHub Pages](https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417)

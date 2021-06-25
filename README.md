# Rancher Helm Chart Testing

## Instructions

### Add charts

#### Amazon Elastic Block Store (EBS) CSI driver

```sh
helm repo add aws-ebs-csi-driver https://kubernetes-sigs.github.io/aws-ebs-csi-driver
helm repo update
helm pull aws-ebs-csi-driver
tar -xf aws-ebs-csi-driver*.tgz
helm lint aws-ebs-csi-driver/*
```

#### Rancher

```sh
helm repo add rancher-latest https://releases.rancher.com/server-charts/latest
helm pull rancher-latest/rancher
tar -xf rancher-*.tgz
helm lint rancher/*
```

### Update Index

```sh
helm repo index --url https://github.com/oxr463/rancher-helm-chart-testing .
```

## Reference

- [Create a public Helm chart repository with GitHub Pages](https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417)


# K3S / Rancher for Local Development

## Requirements

Installs:

- [Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
- [k3s](https://k3d.io/v5.7.4/#installation)

## Terraform

- Init Terraform: terraform init
- Plan: terraform plan
- Execute and create: terraform apply

### Deploy applications to local cluster

```shell
kubectl apply -f path/to/your/manifests/
```

### Config kubectl to connect into the cluster

- Get kubeconfing from k3s cluster

```shell
export KUBECONFIG=$(k3d kubeconfig write k3s-cluster)
```

- Bind kubectl to kubeconfig

```shell
kubectl get nodes
```

### Other tools

- k3d: To manage clusters k3s on Docker.
- kubectl: To interact with k8s cluster,
- Terraform k3d provider: Easily create clusters k3s with Terraform.

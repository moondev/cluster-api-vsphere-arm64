# cluster-api-vsphere-arm64
cluster-api vsphere workload clusters on esxi for arm

The following machine image is built from Photon OS 4.0 arm64 OVA, and includes:
* `kubeadm`, `kubelet`, `kubectl` v1.21.2
* `containerd` configured with systemd cgroup driver
* `cloud-init` configured for vmware guestinfo datasource
* `crictl` configured for `containerd` socket

## pre-built machine image
https://cappi.s3.us-west-2.amazonaws.com/kube-v1.21.2-photon-4-arm64.ova

## quickstart
simply import the ova into your esxi on arm vsphere cluster, then initialize a local (x86) capi mgmt cluster via `kind`. Once mgmt cluster is up, create workload cluster with the machine image.

## Introduction

These scripts is based on kubeadm, which can help you bootstrap a minimum viable Kubernetes cluster that conforms to best practices. With this script, you can support cluster lifecycle functions, such as upgrades, downgrade, and managing bootstrap tokens.

## Create cluster with singleton model

1. install kubernetes with network plugin "calico"

```
/usr/share/openvswitch/scripts/ovn-ctl start_northd
/usr/share/openvswitch/scripts/ovn-ctl start_controller
ovnkube -k8s-kubeconfig /etc/kubernetes/admin.conf -net-controller \
 -loglevel=4 \
 -k8s-apiserver="http://$CENTRAL_IP:8080" \
 -logfile="/var/log/openvswitch/ovnkube.log" \
 -init-master=$NODE_NAME -init-node=$NODE_NAME \
 -cluster-subnet="$CLUSTER_IP_SUBNET" \
 -service-cluster-ip-range=$SERVICE_IP_SUBNET \
 -nodeport \
 -init-gateways -gateway-localnet \
 -k8s-token="$TOKEN" \
 -nb-address="tcp://$CENTRAL_IP:6641" \
 -sb-address="tcp://$CENTRAL_IP:6642"
```

- A cluster wide private address range of $CLUSTER_IP_SUBNET (e.g: 192.168.0.0/16). The pods are provided IP address from this range.

- $NODE_NAME should be the same as the one used by kubelet. kubelet by default uses the hostname. kubelet allows this name to be overridden with --hostname-override.

- $SERVICE_IP_SUBNET is the same as the one provided to k8s-apiserver via --service-cluster-ip-range option. An e.g is 172.16.1.0/24.

- $TOKEN: kubectl describe secret $(kubectl get secret -n kube-system | grep default-token | awk '{print$1}') -n kube-system | grep "token:" |awk -F"token:" '{print$2}'

2. then you can see the following commnad line instructions

```



## Demos

please see https://github.com/kubernetes/examples

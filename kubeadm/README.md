This version is Just for CentOS 7.x

## What is kubeadm

kubeadm can help you bootstrap a minimum viable Kubernetes cluster that conforms to best practices. With kubeadm, your cluster should pass Kubernetes Conformance tests. Kubeadm also supports other cluster lifecycle functions, such as upgrades, downgrade, and managing bootstrap tokens.

## How to use kubeadm

1. modify your hostname if it's name equal 'localhost'. otherwise, you can skip this step.

```
bash scripts/setHost
```

2. install kubernetes with network plugin "calico"

```
bash setCluster
```

3. then you can see the following commnad line instructions

```
You should now deploy a pod network to the cluster.
Run "kubectl apply -f [podnetwork].yaml" with one of the options listed at:
  https://kubernetes.io/docs/concepts/cluster-administration/addons/

You can now join any number of machines by running the following on each node
as root:

  kubeadm join 118.190.96.247:6443 --token 7br8a7.592ei2vq32n0hobm --discovery-token-ca-cert-hash sha256:7c0f3d52670e6e64e7cce7f700b46e88154dc4bf94bf82938488e13eb49b4b31

......

http://[IP]:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/
W0916 21:20:46.005078   31923 proxy.go:139] Request filter disabled, your proxy is vulnerable to XSRF attacks, please be cautious
Starting to serve on [::]:8001
```

4. visit the below URL and click the skip button. That is all, please enjoy it.

```
http://[IP]:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/
```

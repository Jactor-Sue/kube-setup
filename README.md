## Background

Cloud computing is one of the most important technologies for enterprises to optimize their IT systems. Although current cloud computing is a foundation for digital business, but it still has flexibility and performance problems. We argue that decouple the control plane from program control flow in cloud computing can take into account both flexibility and performance. Then we design a software defined cloud (SDC) system. Here, This project is used to provide a simple way to install SDC, and we have the following assumptions (please install them by yourself):

- Docker: please see the guide to get docker-ce for different Linux distributions, such as [redhat](https://docs.docker.com/install/linux/docker-ee/rhel/), [SUSE](https://docs.docker.com/install/linux/docker-ee/suse/), [Oracle Linux](https://docs.docker.com/install/linux/docker-ee/oracle/),[centos](https://docs.docker.com/install/linux/docker-ce/centos/), [debian](https://docs.docker.com/install/linux/docker-ce/debian/), [fedora](https://docs.docker.com/install/linux/docker-ce/fedora/), [ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- Openssl:[OpenSSL](https://www.openssl.org/) is a robust, commercial-grade, and full-featured toolkit for the Transport Layer Security (TLS) and Secure Sockets Layer (SSL)
- socat: [socat](http://www.dest-unreach.org/socat)is a relay for bidirectional data transfer between two independent data channels.

## Systems

- [PublicCloud Controller](kubepubcloud/README.md): Mist helps you manage and monitor your computing infrastructure, across multiple clouds and platforms.
- [Container Controller](kubernetes/README.md): Kubernetes is an open-source system, which can be used as container controller for automating deployment, scaling, and management of containerized applications.
- [ServiceMesh Controller](kubeservices/README.md): istio is an open-source system, which can be used as servicemesh controller to Connect, secure, control, and observe services.

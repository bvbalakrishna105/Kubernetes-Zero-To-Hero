# What is kubernetes ?

As per wikipedia defination 
Kubernetes, commonly abbreviated K8s is an open-source container orchestration system for automating software deployment, scaling, and management. Originally designed by Google, the project is now maintained by the Cloud Native Computing Foundation (CNCF).

# What kind of problems k8s going to address it?

1. Single node host(s) in nature
2. Auto Scaling is not there 
3. Auto Healing is not there
4. Docker is not enterprise solution

# What is kuberneters Cluster Architecture and each components ?

K8s are broadly divided into two catogeries
1. Control Plane (master/primary)
2. Data Plane (slave/standy/secondary/worker/Node)

In the Data Plane

1. Pod 
    Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.

2. Kubelet
    The kubelet is the primary "node agent" that runs on each node. It can register the node with the apiserver using one of: the hostname; a flag to override the hostname; or specific logic for a cloud provider.

    The kubelet works in terms of a PodSpec. A PodSpec is a YAML or JSON object that describes a pod.

3. Kube-proxy
    The Kubernetes network proxy runs on each node. This reflects services as defined in the Kubernetes API on each node and can do simple TCP, UDP, and SCTP stream forwarding or round robin TCP, UDP, and SCTP forwarding across a set of backends.

4. Container Runtime
    You need to install a container runtime into each node in the cluster so that Pods can run there


In the Control plane

1. Kube-api-server:
    The Kubernetes API server validates and configures data for the api objects which include pods, services, replicationcontrollers, and others. The API Server services REST operations and provides the frontend to the cluster's shared state through which all other components interact.

2. Controller Manager:
    The Kubernetes controller manager is a daemon that embeds the core control loops shipped with Kubernetes.

    In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the apiserver and makes changes attempting to move the current state towards the desired state.

3. Scheduler:
    The Kubernetes scheduler is a control plane process which assigns Pods to Nodes. The scheduler determines which Nodes are valid placements for each Pod in the scheduling queue according to constraints and available resources. The scheduler then ranks each valid Node and binds the Pod to a suitable Node.

4. etcd:
    etcd is a consistent and highly-available key value store used as Kubernetes' backing store for all cluster data.

5. Cloud-Controller-Manager (CCM) (optional): 
    The cloud-controller-manager is a Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.

# What is kubectl ?

Kubernetes provides a command line tool for communicating with a Kubernetes cluster's control plane, using the Kubernetes API.

# What is minikube ?

minikube is local Kubernetes (single node architecture), focusing on making it easy to learn and develop for Kubernetes.

More details: https://minikube.sigs.k8s.io/docs/start/

# Is there any quick reference guide for kubernetes ?
Yes !!! 
kubectl Quick Reference
https://kubernetes.io/docs/reference/kubectl/quick-reference/


# What is replicaset in kubernetes ?

A ReplicaSet's purpose is to maintain a stable set of replica Pods running at any given time. As such, it is often used to guarantee the availability of a specified number of identical Pods.

# What is service in kubernetes ?

In Kubernetes, a Service is a method for exposing a network application that is running as one or more Pods in your cluster.

# What is deployments in kubernetes ?

A Deployment provides declarative updates for Pods and ReplicaSets.

You describe a desired state in a Deployment, and the Deployment Controller changes the actual state to the desired state at a controlled rate.
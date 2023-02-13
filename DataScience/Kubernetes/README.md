## Why Data Scientists needs Kubernetes?

<img align="centre" src="Asset/why,question.jpg" height="600" alt="Why"> 

Data scientists often use [`containerization`]() technologies like [`Docker`]() to package their code and dependencies in a portable and reproducible way. Kubernetes is a powerful tool that can help data scientists manage and orchestrate these containers in a production environment.

Some of the main reasons why a data scientist might use Kubernetes include:

Scalability: Kubernetes allows data scientists to easily scale their applications up or down, depending on the workload. This can be especially useful for handling large data sets or running complex [`machine learning`]() models.

Reliability: Kubernetes can automatically monitor the health of [`containers`]() and automatically replace them if they fail, which can help ensure that data science applications are always available.

Portability: Kubernetes allows data scientists to deploy their applications to different environments, such as on-premises, in the cloud, or in a hybrid environment, without having to change the underlying code or dependencies.

Resources Management: Kubernetes allows to easily manage resources like CPU, memory, and storage for the containers, this can help to optimize the performance of the Data Science workload.

Overall, Kubernetes can help data scientists to manage the deployment and scaling of their containerized applications in a more efficient and reliable way.

## Resources to learn

- [Kubernetes Tutorial for Beginners](https://www.youtube.com/watch?v=KVBON1lA9N8) - [Kunal Kushwah]() 

- [Kubernetes 101 workshop](https://youtu.be/PN3VqbZqmD8) - [Kubesimplify]

## What is Kubernetes?

<img align="centre" src="Asset\Kubernetes img.png" height="500" alt="Why"> 


`Kubernetes` is an open-source platform that helps to manage and [`orchestrate`]() containerized workloads and services. It is a system that automates the deployment, scaling, and management of containerized applications.

In simple terms, Kubernetes is like a traffic controller for your containers. It makes sure that your containers are running as they should, and if one of them fails, it will automatically start a new one. It also allows you to easily scale your applications up or down, depending on your needs.

This platform can run on-premises or in the cloud, and it makes it easy for organizations to deploy, scale and manage containerized applications in a consistent and predictable way.


## Kubernetes Components

<img align="centre" src="Asset\components-of-kubernetes.svg" height="500" alt="Why"> 
<!-- Don't correct grammatical mistake of above kubernetes  -->

This section is under maintainance.
> You can raise issue to work on it 



## NameSpace

This provide a isolated environmnet within a sigle cluster

Note
> Resources names must be distinct both within and between namespace,but not across other namespaces.


## Initial Namespaces

`default`

Kubernetes includes this namespace so that you can start using your new cluster without first creating a namespace.

`kube-node-lease`

This namespace holds Lease objects associated with each node. Node leases allow the kubelet to send heartbeats so that the control plane can detect node failure.

`kube-public`

This namespace is readable by all clients (including those not authenticated). This namespace is mostly reserved for cluster usage, in case that some resources should be visible and readable publicly throughout the whole cluster. The public aspect of this namespace is only a convention, not a requirement.

`kube-system`

The namespace for objects created by the Kubernetes system.

Note 
> Reference : [Kubernetes](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)


### Start with Namespace

You can this following commond to check the status of the current namespaces in a cluster you are using : 

cmd:

```yaml

controlplane $ kubectl get ns
```

O/P:

```yaml

NAME              STATUS   AGE
default           Active   35d
kube-node-lease   Active   35d
kube-public       Active   35d
kube-system       Active   35d
```

Now to create namespaces:

```yaml

kubectl create namespace <name>
kubectl create namespace dev

```
for example

```yaml

kubectl create ns dev
kubectl create ns testing
kubectl create deploy yash --image=nginx
kubectl create deploy yash --image=nginx -n dev


```


## Labels and Selectors


Labels are key value pairs that are attached to objects such as pods.

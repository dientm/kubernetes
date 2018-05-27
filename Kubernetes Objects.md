# Kubernetes Objects

## Pods

- A Pod is the basic building block of Kubernetes–the smallest and simplest unit in the Kubernetes object model that you create or deploy. A Pod encapsulates an application container (or, in some cases, multiple containers), storage resources, a unique network IP, and options that govern how the container(s) should run. A Pod represents a unit of deployment: a single instance of an application in Kubernetes, which might consist of either a single container or a small number of containers that are tightly coupled and that share resources.

- Like in Docker, container is the smallest unit, in k8s Pod is the smallest unit.

- Pod is a wrapper around container in k8s.

- You can run single container or multi-container inside a Pod

- Pods do not, by themselves, self-heal. If a pod is scheduled to a Node that fails, or if the scheduling operation itself fails, the Pod is deleted.

## Replica Controller

- Also knows as rc/rcs

- A ReplicationController ensures that a specified number of pod “replicas” are running at any one time.

## Deployment

- A Deployment provides declarative updates for Pods and ReplicaSets (the next-generation ReplicationController).

- You describe a desired state in a Deployment object, and the Deployment controller changes the actual state to the desired state at a controlled rate. You can define Deployments to create new ReplicaSets, or to remove existing Deployments and adopt all their resources with new Deployments.

- Replica Controller is old way to manage the desired state of the pod.

## Services

- Service is all about exposing your application to outside world.

- A Kubernetes Service is an abstraction which defines a logical set of Pods and a policy by which to access them from outside world.

- Let say there is a pod running your web application, to expose this web application you need services.

- It gives you a way to access your Pods, load balancing among your Pods.

- It hides how it manages the Pods internally.

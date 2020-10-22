# Introduction

## Building an Istio 1.6 Service Mesh for Bee Travels, a Microservices Based Application Deployed on Kubernetes

In this code pattern, we will deploy a microservices based application to IBM Kubernetes Service and create a service mesh with Istio 1.6.

When you have completed this code pattern, you will understand how to:

* Deploy a microservices application on Kubernetes
* Configure an Istio service mesh, including:
  * Install and configure the IBM Managed Istio add-on
  * Route traffic to specific microservice versions
  * Shift traffic between multiple microservice versions \(A/B testing\)
  * Access distributed trace spans through Jaeger
  * Analyze service traffic and latency through Grafana
  * Visualize the service mesh through Kiali
  * View access logs 
* Generate load tests with [Artillery](https://artillery.io/docs/)

## Steps

1. [Complete the IBM Cloud set-up for Kubernetes and Istio](./#1-Complete-the-IBM-Cloud-set-up-for-Kubernetes-and-Istio)
2. [Clone the repository](./#2-Clone-the-repository)
3. [Deploy the application to Kubernetes](./#3-Deploy-to-Kubernetes)
   * Deploy version 1 \(data stored in json flat files\)
   * Deploy version 2 \(data stored in an in-cluster database\)
   * Deploy version 3 \(data stored in a database in the cloud\)
   * Access the application \(ingress gateway\)
4. [Configure the Istio service mesh](./#4-Configure-the-Istio-service-mesh)
   * Route traffic to specific microservice versions
   * Shift traffic between multiple microservice versions
   * Access distributed trace spans through Jaeger
   * Analyze service traffic and latency through Grafana
   * Visualize the service mesh through Kiali
   * View access logs

### 1. 

### 2. 3. 4. 

### License

This code pattern is licensed under the Apache License, Version 2. Separate third-party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1](https://developercertificate.org/) and the [Apache License, Version 2](https://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache License FAQ](https://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)


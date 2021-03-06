Kubecost supports the ability to view cost and health data across multiple Kubernetes clusters and cloud providers. 
Below are the steps for adding an additional cluster to your Kubecost frontend.

**Steps**

1. Install Kubecost on the additional cluster you would like to view. The recommended Kubecost install path is available at [kubecost.com/install](http://kubecost.com/install). 
2. Expose port 9090 of the `kubecost-cost-analyzer` pod. This can be done with a Kubernetes ingress ([example](https://github.com/kubecost/docs/blob/e82db0bff942dbb8abf6d74b979b10b121bce705/getting-started.md#basic-auth)) or loadbalancer ([example](https://github.com/kubecost/docs/blob/master/kubecost-lb.yaml)). **Warning:** by default a LoadBalancer exposes endpoints to the wide internet. Be careful about following the authentication requirements of your organization and environment. 
3. Select Add new cluster on the Kubecost home page and provide the accessible URL (with port included) for the target Kubecost installation. Here's an example: `http://e9a706220bae04199-1639813551.us-east-2.elb.amazonaws.com:9090`

![Add a cluster view](kubecost-index.png)

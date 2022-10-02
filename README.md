# gke-ingress

The repo contains 2 helm charts to demo GKE Ingress.

##### Deploy Host based GKE ingress
To see how hostname based routing works in GKE ingress, please deploy web_based_ingress helm chart using below command

```bash
helm install host-based-ingress ./web_based_ingress --namespace <namespaceName>
```

##### Deploy GKE ingress with custom backend and frontend configuration 
To see how we can configure backend service configuration and Ingress frontend configuration via kubernetes objects, deploy customize_ingress helm chart.
<br>

<b> Pre-requisites to install customize_ingress helm chart </b>

<ol> <li>Create a self managed certficate in the project named testgke
<li>Reserve an external IP address named gke-test-self
</ol>

Now install the helm using below command:
```bash
helm install customize-ingress ./customize_ingress --namespace <namespaceName>
```

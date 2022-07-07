# Setting up simple application that utilize nginx contraoller to route request using ingress resource definition
# Docker desktop setup to utilize ingress controller based on resource definition to route request

1. Setup nginx-controller
   kubectl apply -f nginx-controller.yaml
   
   Reference: https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.1/deploy/static/provider/baremetal/deploy.yaml

2. Change the service type of nginx-controller from NodePort to Loadbalancer to expose lower port

3. Deploy application to kubernetes
   kubectl apply -f nginx-manifest.yaml


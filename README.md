# istio-boilerplate
This project is a Istio configuration files template that can be used to kickstart an istio based Kubernates system.
This boilerplate supports the most important entities that can be used like gateways, virtual services, databases services, deployments and volumes ... etc.
Also it supports a basic template for implementing authentication interceptor for specific backend services.
## Some Concepts and Definitions
### Service
A service definition is the configuration file that generates a Kubernates service inside the Kubernates cluster, we can define a name for a service, a port which the service works on and much more. Each service we has a deployment that configure how we are fethcing the container instances to deploy the service, how many pods we want to define for each service and much more.
A volumes is defined in case there is a service that wants to store a presistant data.
You can return to Kubernates website for further info [https://kubernetes.io/docs/home/]
### Virtual Service
### Gateway
### Authentication Interceptor
Istio supports authentication through Envoy filters which uses JSON Web Token (JWT) as defined by RFC 7519. For more info about authentication policy in Istio you can return to Istio docs from [https://istio.io/docs/reference/config/istio.authentication.v1alpha1/].
Envoy filter can be configured with custom Lua code that may connect to any RESTful end point to authenticate the request and extend the headers of the request going to the service with some info like the user id, company id, roles name ... etc.
Inside auth folder there is a template to configure the Envoy filter for custom authentication.
### How to use these configuration files

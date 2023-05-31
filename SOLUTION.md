### The deployment runs a Docker container, what container does it run and what version?

> It returns as nginx container, version 1.25.0-alpine.

### Where do you think Kubernetes "pulls" this image from?

> From the docker repository.

### The deployment.yaml defined a property called replicas. What do you think this means?

> This indicates how many pods are created, and thus how many individual containers. They are called replicas because they are all based on the same image.

### You had to increase the amount of pods running NGiNX, what command did you use to check the amount of running pods and what did it output?

> I used the 'kubectl get pods' command. After I changed the number of replicas to 6, it outputted the following:

```
NAME                        READY   STATUS    RESTARTS   AGE
my-nginx-65c759bdfb-8cp7m   1/1     Running   0          20m
my-nginx-65c759bdfb-8ndnw   1/1     Running   0          22m
my-nginx-65c759bdfb-dslcj   1/1     Running   0          20m
my-nginx-65c759bdfb-hxvds   1/1     Running   0          22m
my-nginx-65c759bdfb-swjjx   1/1     Running   0          20m
my-nginx-65c759bdfb-v5grc   1/1     Running   0          22m
```

### In the service.yaml, it had the identify which pods to send traffic to - which part of the service.yaml defined this?

> This was in the 'ports' block, which defines the protocol type (in this case TCP), the local port (3000), and the target port, which the the port the containers will be listening on (80).

### Screenshot of the Node API server running through a kubernetes cluster:

![Screenshot of the Node API server running through a kubernetes cluster](./kubernetes-myapp/Screenshot%20from%202023-05-31%2016-12-17.png)

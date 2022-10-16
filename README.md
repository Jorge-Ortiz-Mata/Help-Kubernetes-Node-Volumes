# Kubernetes and Node API.

This is simple web application where users can add stories to the story folder(ignored by git).
This application is launched using Docker and Kubernetes.
THe purpose of this application is to save the data given by the user with Kubernetes.

## Getting Started.

In Kubernetes, you have to define all the resources you need for your project.
You can have:
  - Deployments.
  - Services.
  - Volumes.

### 1. Installation.

You have to install **kubectl** and **minikube** in your local machine to be able to launch the kubernetes dashboard. You can install a virtual machine or use docker to create a container where you can have your dashboard.

Once you have installled the two requirementes above, run the next command to crearte the Docker Containers.

```
minikube start --driver=docker
```

Wait until the Docker Container is ready. You can launch the minikube dashboard by running the following command:

```
minikube dashboard.
```

### 2. Kubernetes online.

You can now run kubernetes commands on the local machine. You can get all your deployments, pods, services, volumes, etc. These are some of the Kubernetes commands:

  - Get deployments: `kubectl get deployments`.
  - Get pods: `kubectl get pods`.
  - Get services: `kubectl get services`.
  - Get volumes: `kubectl get pv`.
  - Get volumes claims: `kubectl get pvc`.

### 3. Initialize Kubernetes pods.

You have to configure your service first, and then, you can deploy your app to be accessible using your local browser.
Get your services first, ande run the next command:

`minikube service my_service_name`.

### 4. Volumes and Persistent Volumes.

Volumes can be used in Kubernetes, but for simple volumes, these will be deleted once the pod is eliminated. We can definde Persistent Volumes to maintain our data alive even if the pod is deleted. They use a Persistent Volume Claim where is another configuration in Kubernetes.

### 5. Enviroment variables.

We could also create environment variables in our Kubernetes Cluster. We created a varenv file and in our deployment file we referenced the variables from the previous file.

## Author.

  - Jorge Ortiz.
  - Software engineer.

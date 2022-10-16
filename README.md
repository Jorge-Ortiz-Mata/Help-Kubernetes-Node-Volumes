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

## Author.

  - Jorge Ortiz.
  - Software engineer.

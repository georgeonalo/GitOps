# End to end  Deployment in Kubernetes clusters using Jenkins, GitOps and GitHub Pipeline

### What are we going to achive in this project?
We have an application running in kubernetes, that application is saying *Hello, My Docker project!*, and the magic starts happening when we change the code and push it to github. As soon as you commit the changes, a jenkins job get submitted automatically, builds a new image, pushes the image to Dockerhub, changes the deployment file with the latest image id, the new image automatically gets deployed to the kubernetes cluster using gitops, and our application starts pointing to the new pod.

### What will be covered in this project:
* GitOps Workflow
  * Difference with DevOps Workflow
* Dockerfile and Jenkinsfile Walkthrough
* Jenkins Installation
* Jenkins Jobs Setup
* ArgoCD (GitOps) Installation
* ArgoCD (GitOps) Setup
* Automating GitHub to jenkins using Webhook
* Zero touch end to end (nirvana!)


![image](https://user-images.githubusercontent.com/115881685/209542342-7247a5d7-f6cd-43c0-b419-7d8b82ab7be6.png)

### In Summary GitOps:
* Periodically syncs the running cluster with the desired state in Git Repo
* Works with both vanilla manifest files or Helm charts
* Reduced learning curve than Devops
* Increased security
  * CI (Developer) and CD (Ops) permissions are seperated
* GitOps doesn't mean getting rid of DevOps

Now lets jump in the Github repository first.

![repo](https://user-images.githubusercontent.com/115881685/215599012-c12f4fcc-7ff2-40c3-8d61-1d9f37850885.png)
This is the kubernetescode repository where we have our applicationfile and dockerfile.


![repo 2](https://user-images.githubusercontent.com/115881685/215599843-cb39bd01-d67f-409d-b036-74d09f934678.png)
Our application code is app.py. It is a very simple python program, which is importing the library flask and just returning Hello, Docker project!


![repo 3](https://user-images.githubusercontent.com/115881685/215601234-51d90fb6-7a68-4694-82e4-685522b55f7d.png)
The file requirements.txt list the external library flask, and in this case we are specifically using the version 2.1.0


![repo 4](https://user-images.githubusercontent.com/115881685/215602130-f844cc27-61ae-4476-a4b6-e3ce6ffe84ac.png)
The dockerfile dockerizes that python program and creates a container image. It is using the base python 3.8 docker image, and then its copying over the requirement file running a pip install of the flask. There it is running the python program accepting incoming connection.




 











Click this link for instructions on how to impliment this project: [Tutorial](https://youtu.be/o4QG_kqYvHk)




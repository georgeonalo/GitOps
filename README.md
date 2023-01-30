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

### In Summary GitOPs:
* Periodically syncs the running cluster with the desired state in Git Repo
* Works with both vanilla manifest files or Helm charts
* Reduced learning curve than Devops
* Increased security
  * CI (Developer) and CD (Ops) permissions are seperated
* GitOps doesn't mean getting rid of DevOps















Click this link for instructions on how to impliment this project: [Tutorial](https://youtu.be/o4QG_kqYvHk)




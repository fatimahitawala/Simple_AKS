# Simple_AKS
# This is a Simple Python Form Deployment on AKS
# Creating Python script that will open Name and Email field form
# Storing the values on Database formdata.db
# Creation of Dockerfile and Image from it using command docker build -t python_form .
# Now we need to deploy application using Kubernetes usinf AKS services on Azure
# Creation of deployment.yml which will create two replicas of the pod kubectl apply -f deployment.yml
# Creation of service.yml file which will allow loadbalancer to expose our application on port 80 and this LB will create external IP kubectl apply -f service.yml
# Configuring AKS services on azure by creating new cluster, that will have control plane (agent pool) as I am using kodekloud subscription.
# Once cluster is deployed we have to connect it using connect button, that will az login to subscrition, and get credentials so that config file gets created on and we can use using kubectl connection to AKS
# Now running kubectl apply commands for both deployment and service.yml file
# Pods get created under default namespace and we can successfully access application from external load balancer
# There are some issues I faced like tainded nodes, which will not allow pod to get created on that node, so I have unticked the requirement.

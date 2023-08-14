# kubernetes-the-hard-way
"Kubernetes The Hard Way" is a hands-on guide that deeply explains how Kubernetes components work together. 
## Progress 
My first try was unsuccessful due to the problems starting etcd service on the 7th stage. Although Kelsey uses 3 controller nodes and 3 worker nodes running on ubuntu-2004-lts image and e2-standard-2 compute unit, my free GCP tier couldn't create the resources needed, so I ended up creating 2 instances for each class. And although I always carefully read the code that I execute, I wrongfully assigned a non-existent IP address to the second controller node, which put etcd.service in a loop and no obvious fixes could help this problem. So I decided to start again and this time, I was successful.
Considering that everything before "Compute Instances" was completed earlier, I had a good headstart. 
I've successfully bootstrapped etcd, Kubernetes controllers, and Kubernetes workers. This is a screenshot of one of the running controllers:
![Screenshot 2023-08-14 131154](https://github.com/gidra39/kubernetes-the-hard-way/assets/95176865/a89b3437-7f39-4c16-8041-2fb40a3722dc)
After bootstrapping everything needed, I've provisioned Pod Network Routes and deployed CoreDNS DNS Cluster Add-on, a yaml for which you can find in this repository in the "deployment" folder.
At the end of this practice, I've successfully smoke-tested my Kubernetes cluster, as seen here:
![Screenshot 2023-08-14 134141](https://github.com/gidra39/kubernetes-the-hard-way/assets/95176865/dcfc4f9a-e8ce-4e24-a9e3-42382462277c)
## Conclusion
As a result of practice, I've received great practical knowledge of properly setting up Kubernetes clusters and an understanding of all the vital components of the Kubernetes cluster.

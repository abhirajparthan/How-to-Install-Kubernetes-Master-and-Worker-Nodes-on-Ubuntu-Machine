# What is Kubernetes?
Kubernetes is an open-source system developed by Google, now overseen by the CNCF. It simplifies container orchestration. Thus, developers can build apps without dealing with infrastructure complexities. This system provides container management and scheduling. Users can dictate application behaviors within a cluster. Kubernetes abstracts the underlying infrastructure, streamlining container tasks and application deployment.

----
###### Benefits of Kubernetes
1. Kubernetes is good at managing containers across diverse nodes;
2. Kubernetes is compatible with many public and private cloud infrastructures;
3. Kubernetes allows you to automatically scale your application when it needs more resources to run successfully;
4. Kubernetes self-healing feature automatically restarts failing containers and replaces unhealthy containers.

----
###### Prerequisites
To install Kubernetes on your Ubuntu machine, make sure it meets the following requirements:

     1. 2 CPUs
     2. At least 2GB of RAM
     3. At least 2 GB of Disk Space
     4. A reliable internet connection
If your machine meets the above requirements, you are ready to follow this tutorial. Let’s start with the step-by-step process on how to install Kubernetes on Ubuntu.

----
###### Overall, installing Kubernetes on Ubuntu involves steps such as:

      1. Disabling swap;
      2. Setting up hostnames;
      3. Setting up the IPV4 bridge on all nodes;
      4. Installing Kubernetes components on all nodes;
      5. Installing Docker or a suitable containerization tool;
      6. Initializing the Kubernetes cluster;
      7. Configuring Kubectl and Calico;
      8. Adding worker nodes.
-----
###### Created A Bash Script for Master Node and Worker Nod.
I have Created a .sh files for installing the Cluster. The one is Master-Node.sh for Master Node. The 2nd One is Worker-Node.sh for worker Nodes. I have attached the .sh Files in the Repository. You can refer this.
.sh Files are Master-Node.sh and Worker-Node.sh

----
###### Add worker nodes to the cluster
Once you have configured the master node, you can add worker nodes to the cluster. When initializing Kubeadm on the master node, you will receive a token that you can use to add worker nodes.

To add the worker nodes to the Kubernetes cluster, use the kubeadm join command. (It looks like this below command. You can get the variable values from the above steps)

~~~
kubeadm init --pod-network-cidr=10.10.0.0/16
~~~
You will get Joint Tocken from the console and Its looks like below image.

![Screenshot from 2023-12-20 14-43-59](https://github.com/abhirajparthan/How-to-Install-Kubernetes-Master-and-Worker-Nodes-on-Ubuntu-Machine-Using-Bash-Script/assets/100773790/b05f1444-bed3-4eb6-895d-ac25199e4f7c)

PLease run the Joint tocken in the Worker-Node server.

Then run the below command in the Master node and you will get the inforamtion about the nodes and It will active state.

~~~
kubectl get node 
~~~

![Screenshot from 2023-12-20 14-49-39](https://github.com/abhirajparthan/How-to-Install-Kubernetes-Master-and-Worker-Nodes-on-Ubuntu-Machine-Using-Bash-Script/assets/100773790/5dc75644-a7fd-49a3-a33c-4eb1dcf6f617)

Here you can see my master node and worker nodes are activate state. 


###### 
## Conclusion
This guide covered how to install Kubernetes on Ubuntu Machines and set up a cluster. By following these steps, you can create a reliable cluster. Kubernetes offers a dependable platform for deploying microservice applications, making it essential for competitive businesses.

---
### ⚙️ Connect with Me

 <p align="center">
<a href="mailto:aparthan275@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://www.instagram.com/_r.e.b.e.l.z_33/"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/abhiraj-parthan-82038b191"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a> 
<a href="https://www.wppredirect.tk/go/?p=918893532145&m=Abhiraj%20Parthan."><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/></a>
  </a></p>
</div>



### K8S - kubernetes base knowledge


Node is Virtual or physical machine
<pre>  
There are 2 types of nodes: 
"master" - manager node-it contain api server ,schedualer,controller manager(what happend in the cluster) and backing store.
"slave" - worker nodes contain buisness logice ,they are controlled by the master node. has at least 60% of cpu.
</br>
The thing that connect master and slave nodes inside of the cluster called "Virtual Network".
<pre>

what is k8s pod ? 
 <pre>
Pod is the smallest unit in k8s
it craete a layer on top of the container,k8s can controll,each pod get unique ip adress that comes with k8s (VN) when creating the pod and that ip adress make it possible to them to communicate each other. 
pay attention! pod can die very easly by server failer and more...and whaen you uploude new pod it will have new ip adress
so in order to keep adresses order we will use service.
 </pre>
 
 What is k8s service ? 
 <pre>
service methode is give a static ip adress to pod so even if it die the service process can be relate the new pod adress just as the old one.
In order to get access to your app trow browser you should have EXTERNAL SERVICE ,but in order to get to adress to pod but without premmision to acces trow browser
(just like DB premission) we will use INTERNAL SERVICE.
When we want to get into pod servuce by browser we need to write http//: 123.456.67.89 in order to change this way and get more clear
adress we will use INGRES that convert url string to the right pod ip adress.
</pre>

ConfigMap



<!-- https://www.youtube.com/watch?v=s_o8dwzRlu4  -->

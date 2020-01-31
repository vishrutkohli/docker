---


---

<p><strong>DETAILED ABSTRACT</strong></p>
<p>The whole workshop will be based on Docker and Kubernetes understanding and how it can be used to make lives of python developers easier.</p>
<p><strong>1.)What and Why’s of Docker?</strong></p>
<p>Explaining the people the hardships they face to run other persons code on their local machine. How docker is helping in eradicating this process of.</p>
<blockquote>
<p>Downloading the installer or setup script —&gt;run the installer or setup script —&gt;an error throws up —&gt;troubleshoot the issue —&gt;Download the dependency —&gt;Run the installer again.</p>
</blockquote>
<p>It is so much easier to go with docker instead of going through the setup procedure without worrying about the dependencies.</p>
<p><strong>2.)what all consists of Docker Ecosystem?</strong></p>
<p>Explaining the different things in the Docker Ecosystem.</p>
<blockquote>
<p>-Docker Server/Demon<br>
-Docker Client<br>
-Docker Machine<br>
-Docker Images<br>
-Docker Hub<br>
-Docker Compose</p>
</blockquote>
<p><strong>3.)How to install and setup docker on your local machine .</strong></p>
<p>Will help the audience to install docker on their laptops.</p>
<p><strong>4.)Sharing a Docker CHEATSHEET which i made which will be used through the course and maybe after that.</strong></p>
<p>This cheat sheet will consist all the basic terms(containers, images etc) which we will use in the workshop with a one liner easy definition. For eg: Docker image- It is a File snapshot which we use to run docker containers.</p>
<p><strong>5.)How does Docker work?</strong></p>
<p>It starts with just running one command <code>Docker run hello-world</code>.</p>
<blockquote>
<p>And then I will explain how Docker CLI understood the command —&gt;explains it to the docker server —&gt;Finding for an image locally cached if not going to docker hub to get the image—&gt;Run the image in the container —&gt;Voila the container is running.</p>
</blockquote>
<p><strong>6.)Basic Docker Architecture.</strong></p>
<p>Explaining the basic architecture of OS</p>
<blockquote>
<p>Running process —&gt; Sys call —&gt; Kernel —&gt; CPU/HDD/Memory.</p>
</blockquote>
<p>So I will explain How containers work on this architecture and how they are better than virtual machines.</p>
<p>I will explain with the help of namespacing and control groups how does this happen and how useful it is.</p>
<p><strong>7.) Explaining what a container Really is and how does an image contributes in setting a container.</strong></p>
<blockquote>
<ul>
<li>how an image Is a file system snapshot .<br></li>
<li>this snapshot is replicated in container shared memory resource. <br></li>
<li>then a new commands runs into the container. <br></li>
</ul>
</blockquote>
<p><strong>8.) Explaining container life cycle</strong></p>
<pre><code>explaining the states a docker container passes through:
&gt;	-Created
&gt;	-Running
&gt;	-Stopped
&gt;	-Paused 
&gt;	-Deleted
</code></pre>
<p><strong>9.)Setting up an already made python-django based project which have a machine learning model converted into a real time API and uses  celery with Redis as a broker and Postgres as a DB.</strong></p>
<p><strong>10.) Writing The dockerfile for the python app and pulling the images of redis and postgres from docker hub.</strong></p>
<p>Explaining the concept of reusability of docker images and starting of the basic structure of a docker file</p>
<blockquote>
<p>——CHOOSE BASE IMAGE<br>
|<br>
|<br>
——INSTALL DEPENDECIES<br>
|<br>
|<br>
——COPY CODE.<br>
|<br>
|<br>
——EXECUTE THE CODE</p>
</blockquote>
<p>And pulling the already made images of Redis and postgressql.</p>
<p><strong>11.) Pushing the image we built to docker hub for further use.</strong></p>
<p><strong>12.)What are Docker Volumes and why do we need it.</strong></p>
<p>Explaining how copying the code does not accommodate the changes you do in your local repo. We will solve this problem step by step by using docker volumes.</p>
<p>#AT THIS POINT THE AUDIENCE WILL BE COMFORTABLE WITH DOCKER AND ITS APPLICATIONS</p>
<p><strong>13.)We have 3 containers running what should i do ? Do you expect to run like this in production?</strong></p>
<p>ABSOLUTELY NOT. We Have to think of a way to orchestrate our containers to run them independently and in a full proof manner.</p>
<p><strong>14.)What and Whys of KUBERNETES!!</strong></p>
<p>We will start with older services like AWS beanstalk and how it increases cost as your application starts to scale. And how with the help of Kubernetes we can solve this problem.</p>
<p><strong>15.)Sharing a Kubernetes CHEATSHEET which i made which will be used through the course and maybe after that.</strong></p>
<p>This will be the same as docker cheatsheet. Explaining basic stuff like with a small one liner explanation. For example, pods, services, load balancer etc.</p>
<p><strong>16.)Kubernetes Architecture explanantion.</strong></p>
<p>Will explain the the  whole MASTER-NODE ARCHITECTURE and how master has the control over all the nodes and why is this needed.</p>
<p><strong>17.) How to set up Kubernetes? in Local and production.</strong></p>
<p>Will explain step by step procedure to setup Kubernetes and how it the setup will be different for local and production.</p>
<p>For local setup we will use something like Minikube and for production I will explain about the managed solutions such as GKE(google Kubernetes engine) and EKS(Elastic Kubernetes service).</p>
<p><strong>18.)What is a pod and how is it different from a container.</strong></p>
<p>Will explain the unit POD which is the smallest unit of Kubernetes. A pod can run multiple containers inside it but it is highly recommended to put two containers in the same pod only if they are highly coupled And how does it help to ensure data locality. Will use some examples to explain this concept.</p>
<p><strong>19.)How to wrote a config file for Kubernetes.</strong></p>
<p>We will start of with getting familiar with some of he basic kubectl commands.<br>
Explaining the different files of Config files we we are going to make in the workshop<br>
BASIC STRUCTURE OF ANY CONFIG FILE . YAML</p>
<blockquote>
<p>APIVERSION:<br><br>
KIND:<br><br>
METADATA:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;      NAME:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;     LABELS:<br><br>
SPEC:<br></p>
</blockquote>
<p>As we can see the first thing we provide to the config file is to use which API VERSION we are going to use and we decide the API VERSION on what KIND(The next field after APIVERSION) of config file we are going to write.</p>
<p>For eg:<br>
Apiversion:v1 has the following kinds</p>
<p>1.)component status<br>
2.)configmap<br>
3.)namespace<br>
4.)event<br>
5.)pods<br>
6.)endpoints<br>
Etc</p>
<p>A-inversion:apps/v1 has the following kinds<br>
1.)controller revision<br>
2.)Stateful Set</p>
<p><strong>20.)What are the kinds of config we are going to use in this workshop. -pods, service and deployments.</strong></p>
<p>Giving a brief overview of PODS, SERVICES and DEPLOYEMENTS.(AS PER THE CHEATSHEET) and make a basic pod(running the Django project) and service(EXPOSING THIS POD TO THE WEB) and explain there work.</p>
<p><strong>21.)Deep dive into pod config.</strong></p>
<p>Explaining each and every thing written in the config file</p>
<p>It will be in the format</p>
<blockquote>
<p>APIVERSION:<br><br>
KIND:<br><br>
METADATA:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	NAME:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	LABELS:<br><br>
SPEC:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	CONTAINERS:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;		NAME:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;		IMAGE:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;		PORTS:<br></p>
</blockquote>
<p><strong>22.)Deep dive into Service config.</strong></p>
<p>The sole part of any service is to create some kind of networking and that’s what I am going to explain in this section.</p>
<p>We are going to learn a very brief details of different kinds of services such as : Nodeport, ClusterIP, LoadBalancer, INGRESS but we will use only  nodeport and clusterIP.</p>
<p>Explaining each and every thing written in the config file</p>
<p>It will be in the format</p>
<blockquote>
<p>APIVERSION:<br><br>
KIND:<br><br>
METADATA:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	NAME:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	LABELS:<br><br>
SPEC:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	TYPE:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	PORTS:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	SELECTOR:<br></p>
</blockquote>
<p><strong>23.) What is the difference between imperative and declarative deployments.</strong></p>
<p>Now talking about to types of deployments One(IMPERETIVE) is in which we have to to explicitly tell what steps to be taken to make any changes and the other(DECLARATIVE) is you rely on the MASTER  to do everything and you just pass your high level command to master.</p>
<p>Will explain why we have to get use of both. And will give an example of both.<br>
For imperative :</p>
<p>How to update the pods when there is no change in the config files but your docker image is updated.</p>
<p>FOR DECLARATIVE:<br>
ANY BASIC KUBECTL COMMAND LIKE  applying a config file</p>
<p><strong>24.)What is a deployment and why do we need it.</strong></p>
<p>So we will be pretty familiar with pods at this point of time. But now we are in a problem. What if due to some circumstances we have to change the port of our POD. But according to the properties of the pod we can’t change it. To solve that problem deployments come into play.  A Deployment can help you to run multiple pods into a single deployment and can help you to modify everything inside a pod because it will just kill that pod and make a new one. So that you are not modifying the pod you are making new ones and killing the ones you don’t want to use.</p>
<p>After this we will write a deployment file to run our Django project pod as a deployment and change its ports.</p>
<p>Explaining the basic structure of deployment config.</p>
<blockquote>
<p>APIVERSION:<br><br>
KIND:<br><br>
METADATA:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	NAME:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	LABELS:<br><br>
SPEC:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;	REPLICAS:<br><br>
TEMPLATE:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;		METADATA:<br><br>
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;		SPEC:<br></p>
</blockquote>
<p>Will the specification in a deployment file work in the form of templates and we can add a number of pods in one deployment.</p>
<p><strong>25.)Do we really need a service?</strong></p>
<p>YES WE ABSOLUTELY DO!!<br>
Cause whenever we do a deployment deploys our container into a pod and that pod gets up and running In a node and that node have an IP now we can’t access that IP on the chrome to access our application endpoint and even if you forward the port on the pod and make publicly accessible what if that pod gets broken and KUBERNETES for you creates a new pod which which will have a different IP.</p>
<p>But you connected and made the port accessible on the pod which no longer exists and your application breaks.</p>
<p>So that’s why we use selector in the services to make connections so that even if the pod does and Kubernetes creates a new one for us still our application works.</p>
<p>THATS THE IMPORTANCE OF SERVICES.</p>
<p><strong>27.)Why we don’t use nodeport in production ? Nodeport vs clusterIP.</strong></p>
<p>I will explain it with a little example.<br>
So when we talk about production it means anyone in the world can access it and even people who do like your app. So you always have to be prepared from the security point of view. So  what cluster IP does is it will only make your service accessible inside the cluster and you cannot access the service if you are trying to use it from the outside. This increases security and that’s why we don’t use nodeport in production .</p>
<p><strong>28.)What are Kubernetes Volumes.</strong></p>
<p>PODS are shot lived. If a pod gets killed the master in Kubernetes will spin up another one. We don’t have to care about this. But what we care about is the data that pod had which will be lost when the pod is killed. So that’s why we make Kubernetes volumes so that even when the pod is killed we do not lose the data and the new pod will also use the same memory source to store and read data.</p>
<p>We will deep dive into persistent volumes and volumes .<br>
To give a brief overview. Volume resides inside the pod so whenever the pod is killed volume also gets killed.</p>
<p>In comparison a persistent volume resides outside the pods so it solves our purpose of data retention.</p>
<p><strong>29.) Defining environment variables(Postgres password) and passing them as secrets.</strong></p>
<p>So as we know Redis and Postgres needs some environment variables to be set to work properly which might have some passwords which we do not want to share with everyone who have access to the Kubernetes cluster.</p>
<p>We will be using<br>
Object type: SECRET and there are two ways to run objects either you use declarative commands like making a config file or you can use an imperative command .<br>
If we are using a config file for this. Than it defeats the main purpose of creating a secret because you had to write the secret in plain text.</p>
<p>So that’s why we are going to use an imperative command:</p>
<p><code>Kubectl create secret generic &lt;secret_name&gt; —from-literal key=value</code></p>
<p>I will explain each word in this command what it is doing .</p>
<p><strong>30.)USING LOAD BALANCER OR INGRES TO HANDLE TRAFFIC and finally starting our application.</strong></p>
<p>We will make our last config file which take the requests from the end point and then split it in our deployment infrastructure. The config file will be similar to the above config files and after applying it we are good to go to use our python web application on Kubernetes.</p>
<p><strong>31.)Playing around with our app on Kubernetes.</strong></p>
<p>Checking the functionalities of the web app and playing around like killing pods giving excess traffic by using prepaid scripts. And checking how our deployment react.</p>
<p><strong>32.)Doing Local development with the help of scaffold.</strong></p>


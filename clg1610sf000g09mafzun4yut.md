---
title: "Deploying Web App using Nginx web server and Reverse proxy🔀"
datePublished: Mon Apr 03 2023 18:29:14 GMT+0000 (Coordinated Universal Time)
cuid: clg1610sf000g09mafzun4yut
slug: deploying-web-app-using-nginx-web-server-and-reverse-proxy
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680546211349/32ec7757-5fa1-421e-9280-62abfd405c8d.webp
tags: aws, nginx, devops, wemakedevs, 90daysofdevops-devops-projectdevelopment-nonitbackground-github-docker-cloudplatforms-ec2-aws-elasticbeanstalk-lambdafunctions-devopspipelines-terraform-jenkins-docker-devsecops-scm-git-gitlab-bitbucket-buildtools-griddle-maven-ant-msbuild-monitoringtools-prometheus-grafana-ansible-ai-chatgpt-valueaddition-realworldproblems

---

Web servers and reverse proxies are powerful tools in the DevOps arsenal, providing a range of benefits for web application performance, security, and infrastructure management.

## What is Nginx?

Nginx is a popular open-source web server software that also functions as a reverse proxy, load balancer, and HTTP cache. It is designed to be lightweight, fast, and scalable, making it a popular choice for high-traffic websites and applications.

The web server serves all the static files i.e. the HTML, CSS, and Javascript files to the client i.e. the user.

Nginx can be used as a standalone web server or in combination with other web servers like Apache. It is also commonly used as a reverse proxy in front of application servers like Node.js or Ruby on Rails, to improve performance and scalability by distributing incoming traffic across multiple backend servers.

## Nginx Architecture

![Nginx | Architecture of Nginx | Learn How to Deploy Application in React |  Application Deployment in React | Docker - New Technology](https://1.bp.blogspot.com/-PjnBMTobTNU/X8czpOlkwnI/AAAAAAAAJmo/Ii9PF_g6HTY5SC_pOQOw3NBcVmunP_McwCNcBGAsYHQ/s1161/ll.jpg align="left")

The architecture of Nginx consists of a master process and multiple worker processes, which enable the server to handle large amounts of traffic while distributing the load among multiple child processes.

For example, if a website is hosted on a specific port and experiences a sudden surge in traffic, the website may become overloaded and crash. However, if the website is served through Nginx, the load is distributed among multiple worker processes, preventing the server from becoming overwhelmed and allowing the website to function smoothly.

In summary, Nginx's architecture is built to deliver high performance and scalability, while remaining flexible and simple to configure.

### Reverse Proxy with Nginx

A reverse proxy is a server that receives client requests and forwards them to the appropriate backend server(s) to handle the request. Reverse proxies are commonly used in DevOps to improve web application performance, increase security, and simplify infrastructure management.

Suppose there is a website running on a particular port on the local host and you want it to run on the production without violating security then we can use the reverse proxy to create a bridge and make the port accessible to all the users.

### Load Balancing with Nginx

Load balancing with NGINX involves distributing incoming requests across multiple backend servers to optimize resource utilization and prevent overloading.

NGINX can be used to balance the load for various types of applications, including HTTP, HTTPS, TCP, and UDP. It can also be used to load balance between servers located in different geographical locations.

### Url redirection and caching

URL redirection is the process of forwarding one URL to another.

Caching with NGINX involves storing frequently accessed static content so that it can be served more quickly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676374787084/d78db350-35cd-440d-b567-397760afa083.gif?auto=format,compress&gif-q=60&format=webm align="center")

To deploy a web application using Nginx server and Reverse Proxy on AWS, you will need the following requirements:

1. AWS account: You need to create an AWS account to access the AWS services.
    
2. EC2 instance: You need to create an EC2 instance on which you will deploy your web application. You can select the instance type based on your application requirements.
    
3. Security group: You need to create a security group to allow inbound traffic to the EC2 instance on ports 80 (HTTP) and 443 (HTTPS).
    
4. Nginx installation: You need to install Nginx on the EC2 instance. You can install it using the package manager available on your instance's operating system.
    

Let's install Nginx and see its usage

```bash
sudo apt-get update
sudo apt install nginx
sudo service nginx status 
sudo service nginx restart
```

![Install and configure Nginx | Ubuntu](https://ubuntucommunity.s3.dualstack.us-east-2.amazonaws.com/original/2X/7/7504d83a9fe8c09d861b2f7c49e144ac773f0c0d.png align="left")

Nginx by default runs on port 80, and the above web document is served. This page is been accessed from /var/www/html.

You can check the Nginx configuration files here:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680544015617/bae87ad9-6980-4d98-aa49-4def0213e8bc.png align="center")

Clone the GitHub repository using the command:

```bash
git clone https://github.com/VishalPraneeth/django-notes-app.git
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680544447680/7efc28d7-feb1-4ed0-92d4-9f6f2fccbbc8.png align="center")

Now to install docker, use the command:

```bash
sudo apt install docker.io
sudo systemctl status docker
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680544749777/46537285-d31f-4290-8d96-f5a81287ac27.png align="center")

But you can't build images or run containers until the user doesn’t have access to the docker. So to give permissions use:

```bash
sudo usermod -aG docker $USER
```

When you add a user to the docker group, you give that user permission to run Docker commands without needing to use sudo. This can make working with Docker more convenient and efficient, especially when you need to run Docker commands frequently.

After this reboot the server.

```bash
sudo reboot
```

In the same GitHub repo, we have DockeFile. This is a Dockerfile used to build a Docker image for a Python web application. The base image is Python 3.9. The working directory is set to "/app/backend" and the requirements.txt file is copied to this directory. The pip command is then used to install the dependencies listed in requirements.txt. The rest of the files in the current directory are also copied to "/app/backend". Port 8000 is exposed, which is the default port used by the Django web framework. The CMD instruction specifies the command to run when a container is started from this image. In this case, it runs the Django development server on all network interfaces (0.0.0.0) on port 8000.

```bash
FROM python:3.9

WORKDIR /app/backend

COPY requirements.txt /app/backend
RUN pip install -r requirements.txt

COPY . /app/backend

EXPOSE 8000

CMD python /app/backend/manage.py runserver 0.0.0.0:8000
```

Build the Docker image using the command:

```bash
docker build -t notes-app .
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545181070/726d6eb9-955f-437d-9210-5cf4aba40a30.png align="center")

Once the image has been built successfully, run the container using the command:

```bash
docker run -d -p 8000:8000 notes-app:latest
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545247302/78035853-026a-4b84-95ef-caa2edcc989b.png align="center")

To allow clients to access the application, we aim to implement the reverse proxy concept. Therefore, the Nginx configuration needs to be modified. To do so, navigate to /etc/nginx/sites-enabled.

Next, we will modify the default configuration file to update the settings.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545358179/e73cfd1f-c1e7-4624-ae77-e863f3eb3c15.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545673981/344f011e-8407-403b-9ac7-94113c515713.png align="center")

And after restarting nginx we can see the app running on localhost

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545747693/9412320e-075d-4240-8619-8ab630e72a51.png align="center")

The web application is now accessible, but the functionality to update or delete notes is not available because the backend code does not support storing such data. To resolve this, we need to transfer all static files of the application to the Nginx root folder located at /var/www/html. This will enable access to the files necessary for proper application functionality.

Go to the below-given path to find the folder containing static files and copy to /var/www/html in recursive order

```bash
cd django-notes-app/mynotes/build/
sudo cp -r * /var/www/html/
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680545958449/fdcd51bd-a8a2-45ed-a75b-08e146b456e1.png align="center")

Now we need to update the location /api for the backend page of the server. Go to /etc/nginx/sites-enabled location and update the code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680546017281/d093255d-5a48-4bc8-842d-e8eec9756365.png align="center")

Once you restart Nginx, you can visit the notesapp in your browser and add notes to it successfully. This concludes the deployment of our web application using the Nginx server.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680546135034/6a671cb7-0b43-4538-88b1-dc22adf9202f.png align="center")

### **If you have got the same output as mine, Yu did it🔥**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676377695464/15ba5ac0-24d1-45ba-a9f5-b9941e6e4a76.gif?auto=format,compress&gif-q=60&format=webm align="center")

I'm pinning the GitHub repo link, you can go through the code and understand it.

["Repository"](https://github.com/VishalPraneeth/django-notes-app.git)

### **Guys, you can connect with me on LinkedIn and GitHub**

*Thank you for staying till the end of this project,* *and* ***feedback is appreciated on my blog*** *if you loved it. And yes, All the Best for your project….👍✨*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676386979809/f85946a9-b3ab-4d46-a39b-49cb17feeca2.gif?auto=format,compress&gif-q=60&format=webm align="left")
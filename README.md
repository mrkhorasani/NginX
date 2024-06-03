# NginX
**Nginx** (pronounced "Engine X") is a versatile web server, that acts as a **reverse proxy**, **load balancer**, **mail proxy**, and **HTTP cache**. Here primarily we are going to explore  Nginx as a load balancer. We'll install and configure Nginx on our computer and conduct basic load balancer testing with Django to demonstrate the straightforward process.

Understanding the "**load balancing**" concept is very crucial. It involves distributing incoming network traffic among several backend servers using a load balancer to enhance server performance. This method becomes particularly essential during high-traffic periods when numerous users access our site simultaneously. Throughout this guide, we'll cover installing Nginx and setting it up for **Round-Robin** load balancing.

1. Launch your Ubuntu Terminal and ensure your system is current by executing:\
```
sudo apt-get update
```
2. Install Nginx with the command:\
```
sudo apt-get install nginx
```
3. Validate the installation by accessing your **IP Address** in your browser. A successful installation will **display a default Nginx page**.\
![image](https://github.com/mrkhorasani/NginX/assets/51242725/4f798d3e-4ad3-4f66-b438-8ea8b7528cc0)
 
Proceed to configure Nginx for load balancing. Navigate to the **default Nginx configuration file** on Ubuntu systems located at `/etc/nginx/sites-available/default`.

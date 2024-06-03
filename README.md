# NginX
**Nginx** (pronounced "Engine X") is a versatile web server, that acts as a **reverse proxy**, **load balancer**, **mail proxy**, and **HTTP cache**. Here primarily we are going to explore  Nginx as a load balancer. We'll install and configure Nginx on our computer and conduct basic load balancer testing with Django to demonstrate the straightforward process.

Understanding the "**load balancing**" concept is very crucial. It involves distributing incoming network traffic among several backend servers using a load balancer to enhance server performance. This method becomes particularly essential during high-traffic periods when numerous users access our site simultaneously. Throughout this guide, we'll cover installing Nginx and setting it up for **Round-Robin** load balancing.

1. Launch your Ubuntu Terminal and ensure your system is current by executing:\
``
sudo apt-get update
``
3. Install Nginx with the command:\
``
sudo apt-get install nginx
``
5. Validate the installation by accessing your **IP Address** in your browser. A successful installation will display a default Nginx page.\

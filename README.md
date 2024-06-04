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
 
4. Proceed to configure Nginx for load balancing. Navigate to the **default Nginx configuration file** on Ubuntu systems located at `/etc/nginx/sites-available/default`.
```
sudo nano /etc/nginx/sites-available/default
```
5. Adjust the configuration to enable simple load balancing with Django later. You have the option to either overwrite the existing configuration with this text or comment out the default configuration before pasting. Please make sure to save the changes after copying this configuration into your system's configuration file.\
![image](https://github.com/mrkhorasani/NginX/assets/51242725/bb5a3781-7a11-4a05-9f9b-9750a1279fdf)



> [!IMPORTANT]  
> You can utilize a different name in the upstream command (apart from "www"). Just ensure consistency with the same name in the proxy_pass section. As we'll test load balancing using localhost and port later, the upstream is configured accordingly.

6. After modification it's time to test your nginx configuration file's structure by executing of below command:\
```
nginx -t
```
7. Your running command result has to be like the below, if not it is necessary to recheck your nginx configuration files:\
![image](https://github.com/mrkhorasani/NginX/assets/51242725/06991034-6ac8-4296-b6fc-8508c5ea3f46)

 
8. After modifying and saving the configuration, restart Nginx by executing:
9. 
```
sudo systemctl restart nginx
```

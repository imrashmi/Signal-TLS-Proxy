# Signal TLS Proxy

To run a Signal TLS proxy, you will need a host with a domain name that has ports 80 and 443 available.

1. Install docker and docker-compose (`apt update && apt install docker docker-compose`)
1. Clone this repository
1. `./init-certificate.sh`
1. `docker-compose up --detach`

Your proxy is now running! You can share this with the URL `https://signal.tube/#<your_host_name>` 

For detailed configuration visit below link
`https://signal.org/blog/help-iran-reconnect/`


Detailed Configuration Docs:


Act as a proxy

If you want to help by running a proxy, to get started you only need the following:

  `a.A server with ports 80 and 443 available.`
 ` b.A domain name (or subdomain) that points to the server’s IP address.
  c.The proxy is extremely lightweight. An inexpensive and tiny VPS can easily handle hundreds of concurrent users.`
  
Here’s how to make it work:

1.SSH into the server.
2.Install Docker, Docker Compose, and git:
`sudo apt update && sudo apt install docker docker-compose git`
3.Clone the Signal TLS Proxy repository:
`git clone https://github.com/signalapp/Signal-TLS-Proxy.git`
4.Enter the repo directory:
`cd Signal-TLS-Proxy`
5.Run the helper script that configures and provisions a TLS certificate from Let’s Encrypt:
`sudo ./init-certificate.sh`
6.You will be prompted to enter the domain or subdomain that is pointing to this server’s IP address.
7.Use Docker Compose to launch the proxy:
`sudo docker-compose up --detach`
8.Your proxy is now running! You can share your proxy with friends and family using this URL format: https://signal.tube/#<your_domain_name>

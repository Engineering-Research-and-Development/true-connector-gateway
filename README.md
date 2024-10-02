# TRUE CONNECTOR GATEWAY

This repository contains the needed software to implement a gateway for the connection between Eng True Connector and an internal AAS server.

For a quick reference please refer to the image below

![tcgateway.png](/docs/img/tcgateway.png)

# Deploy
The ecosystem can be deployed with the docker-compose included in this repository.
So, clone the repository using `git clone`, then in the root
```
docker compose up
```
This will expose the AASX-server and a Nginx server which enables locally the URL: `http://tc-gateway.localhost`
This points to the AASX-server, enabling only the GET requests and disabling the others.
The AASX-server API remains the same.

# Add AASX packages
To add new packages, simply copy any new aasx package into the folder `src/aas-source` then run the docker compose.

# Notes
The current configuration relies on "standard" system password to work. 
Please consider to replace these in the src/basyx-conf property files as well as the docker-compose.yml. 
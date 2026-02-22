Let us take a journey to understand different netwroking topics.
ES - Effective Solutions

1. Single server
   IP address - Every machine needs unique address to find the server across internet
   Landing page
   Serve static file on port 80 - http, 443 - https
2. Multiple apps in a server
   Run them on different ports.
   Static frontend assets on port 443.
   backend api = /api - on 8000
   SQL - 306
3. Subnets - Groups
   Fronend services will be inside one subnet
   /api backend services will be inside another subnet
   similarly db
   Subnets can talk to each other. Need to setup firewall rules for access related permissions.
   Only backend need to connect db subnet not the frontend subnet
4. NAT - All the servers inside will have private addresses. But to talk to internet we need a public address.
   All the servers can talk to this NAT. NAT is visible to the outside internet as a public address
5. Cloud - renting infra. We can setup a VPC with multiple subnets.
   Routing needs to be established. Gateways.
6. Container - small unit. Packaged binaries, OS and app.
   Docker is famous for this. Run mutiple containers.
   All the containers can talk to each other using bridge network
   Each container will expose and translate to a port on the machine it is running on.
   That means, when we hit 3000 on local machine, this will reach to the container in which the app code is running and opened on 3000
7. Kubernetes - Pod is the unit.
   Orchestration of containers. Each service has a IP. Mainly we will have ingress, which decides to which service the req should go.
   Multiple services - will have their pods.
   K8s will take care of replacing broke pods.

Video - https://www.youtube.com/watch?v=xj_GjnD4uyI

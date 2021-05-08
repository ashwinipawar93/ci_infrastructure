# jenkins-master                                                                                                                                                                                      
Use following commands to start master containers. There are two seperate containers one for Production Environment and one for Development Environment. 
## Build image
```bash
 $ docker build -t synapticon/somanet-jenkins-master -f Dockerfile .
```
## Start master Contianers
compose files consists of two services(Production & Development)
```bash
 docker-compose up -d    
```

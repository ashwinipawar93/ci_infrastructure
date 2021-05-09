# Slave Containers                                                                                                                                                                                      
Use following commands to start slave containers. There are two seperate containers one for Production Environment and one for Development Environment. 
## Build image
```bash
 $ docker build -t ashpawar/jenkins-slave:3.27-1-alpine -f Dockerfile .
```
## Start Contianer
compose files consists of two services(Production & Development)
```bash
 docker-compose -f slave1.yml up -d 
 ... and so on      
```

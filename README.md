# Continuous Delivery - 
Build a pipeline to shorten the development time needed, and seamlessly transition into Development / QA / Production stages.  Jenkins is deployed as a coordinator using Chef for testing/deployment of our resources.

Our design goals are:  
1. Provide Clean API  
2. Balance consistency & flexibility  
3. Controlled cookbook promotion  

# Chef 
Cookbook types  
1. Library  
2. Application Cookbooks  
3. Data Bags (one per application group) 

Roles  
1. Deployers  
2. Technologist Point Of Contacts  
3. Framework Developer  
![alt text][cookbook]  
_____  
  
# Jenkins
Build Server - for each application group 

1. Cookbook CI job  
..1. Triggered on code merge  
..2. Integration testing  - Test Kitchen  
2. Cookbook Release job  


Deploy Server   

1. Deploy Job
 
![alt text][build]  
_____
Install Jenkins
```* sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
* sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
* sudo yum install jenkins  
```

[cookbook]: https://github.com/ContainerAideR/ContainerAideR-CI/blob/master/img/ci-cookbook-build.png?raw=true "Chef Cookbook"
[build]: https://github.com/ContainerAideR/ContainerAideR-CI/blob/master/img/ci-app-deploy.png?raw=true "Build Server"



# Continuous Delivery - 
Build a pipeline to shorten the development time needed.  Jenkins is deployed as a coordinator using Chef for testing/deployment of our resources.

Our design goals are:  
1. Provide Clean API  
2. Balance consistency & flexibility  
3. Controlled cookbook promotion  

## Chef 
Cookbook types  
1. Library  
2. Application Cookbooks  
3. Data Bags  

Roles
1. Deployers  
2. Tech POC  
3. Framework Developer  

## Jenkins
Build Server - for each application group  
1. Cookbook CI job  
	1. triggered on code merge  
	2. Integration testing  - Test Kitchen  
2. Cookbook Release job  




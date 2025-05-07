youtube clone app deployment usin azure devops , MS osted aent 

followewd steps such as azure repo  and azure pipeline 
steps:

1. create azure repo project import project code

2. setup pipeline pool agent like hosted / self hosted , I used MS hosted agent.


  ![image](https://github.com/user-attachments/assets/faa961e5-81d7-4e99-95a0-ade98c75d734)
  


   ![image](https://github.com/user-attachments/assets/be81a7fe-1c9d-4534-9c4e-e32f50d5349a)


  Each agent ( Agent job 1 ) can do N jobs and each job has N no of tasks , so it is upto our requirement to add no of jobs / tasks , here I was run the pipeline manually to run job 

  ![image](https://github.com/user-attachments/assets/7f0d6cf5-46d0-47cf-b959-918b6a26f6d8)


   ![image](https://github.com/user-attachments/assets/89badcbc-cb5c-469d-b498-f0b7619a8792)


3. create a pipeline , assign tasks to it

   ![image](https://github.com/user-attachments/assets/7c55f48d-61e1-44ea-b489-3086b3eabe32)



4.create a web app using azure app service for deployment of our app 

details : 
 central india region 
Ignore database , disable appllication insights, disable CD deployment , diable virtual network, Tags 


 ![image](https://github.com/user-attachments/assets/3b4e7946-5dcb-4375-8d65-afc58b782728)


 ![image](https://github.com/user-attachments/assets/ce77e034-a4d6-491e-8e13-957b5184470d)
 




























































   

![image](https://github.com/user-attachments/assets/fcb856ba-66a1-4470-b692-185231d8bb2d)

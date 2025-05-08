I have achieved  making automated relaease of youtube application into staging(Dev ) and Prod environments , respectively 

req services : 
  1. two app services for staging(Dev ) and Prod environments.
  2. create two deployment slots



1. create a pipline upto build stage, once build is complete it can generate artifacts for next steps 

![image](https://github.com/user-attachments/assets/2a8f0eb9-703a-4862-b390-8258a75e7122)


2.create a new release ( called youtube_CD )  and upoad artifacts in artifact stage, ( meanning artifacts must be ready if build success ) 
![image](https://github.com/user-attachments/assets/5078a3c0-7dd3-45db-939b-ce302b34fdc6)


3. enable trigger option for Contrinous Deployment ( CD ) from main branch.

   ![image](https://github.com/user-attachments/assets/2577abe0-56a6-4187-add3-57798446b0c4)


4. add a stage called Dev-deployment ( staging ENV )

5. click on pre-deployment conditions, before dev-deploy starts 

   ![image](https://github.com/user-attachments/assets/4b2af63f-629c-4509-bf47-532d898a4446)

6. Click on Tasks Tab
    a) configure deployment properties such as name , app service name, etc 

    ![image](https://github.com/user-attachments/assets/5eaa95fc-50eb-46dd-acc1-888c122c6558)


   b) click on agents tab , name , select pipeline pool , etc

   ![image](https://github.com/user-attachments/assets/4ec11a37-2382-43ca-8a36-3a764ec2cc53)

  c) click on app deploy service , configure below properties ( must select deployment slot as staging else it goes default i'e PROD env ) 

  ![image](https://github.com/user-attachments/assets/ab1e24a3-10a7-4f49-9fcc-6b38847dfd86)


7.create a new called Prod-deployment 

8.for Pre-deployment conditions , make sure that previous stage is passed and Add an approvers ( my name is self added ) 

![image](https://github.com/user-attachments/assets/8c53eebb-780e-4737-bba0-25fa6630b2db)


![image](https://github.com/user-attachments/assets/56540939-f295-4204-958f-ac16aeffe801)

9. click on tasks tab
     a) configure deployment properties such as name , app service name, etc 

   ![image](https://github.com/user-attachments/assets/03dd5732-8faa-4655-bb8c-1b6c53accc06)

     b) click on agents tab , name , select pipeline pool , etc

    c) click on app deploy service , configure below properties ( uncheck deployment slot option as it directly deploys into Prod env default ) 

     ![image](https://github.com/user-attachments/assets/7f38a05d-78ce-4754-be9f-249cf99e97cd)


10. run pipeline , after see the release pipelines stages, automatically it triggers to release

    ![image](https://github.com/user-attachments/assets/0d3b4aaa-aee9-4193-b548-d29d888dd132)



11. first Dev- deployment is passed and we can see app is deployed into staging env ( staging slot )

    ![image](https://github.com/user-attachments/assets/bf5d7285-c7dd-47fe-a07d-8f06240cd883)

    
12 . once we approve , app is also deployed in prod- Environment 

![image](https://github.com/user-attachments/assets/91530723-b978-4040-a818-95ba35a45618)

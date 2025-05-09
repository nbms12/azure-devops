Aim : Deploy using Azure artifacts in azure devops 

req: source code of app, azure devops project , auzre service plan 

Note: You must set the app settings as below to disable all file caching:

WEBSITE_DYNAMIC_CACHE=0
WEBSITE_LOCAL_CACHE_OPTION=Never

import into azure repo : https://github.com/nbms12/nike_landing_page

Arc diagram

![image](https://github.com/user-attachments/assets/3dad9725-90aa-4c7b-92f4-364a95316fdd)


steps: 
1. create web app under azure app service wit free F1 plan , node as run time stack

2. create a feed under azure artifact

![image](https://github.com/user-attachments/assets/bc897f68-6a30-48b7-87ca-2e49112d8736)


3. give permissions to artifact components created earlier as conrtibutor 

   ![image](https://github.com/user-attachments/assets/fe568c1c-4b40-4f30-ad16-7c223145f481)


4.create a pipeline upto build and artifacts stage like below . 

![image](https://github.com/user-attachments/assets/6bcb103c-0dd5-4136-90d1-01fe31a01c60)

5. run pipeline and we can see artifacts are stored in azure artifacts

   ![image](https://github.com/user-attachments/assets/8dad0eb2-6697-490e-a606-193597bb956c)


6. create a new release pipeline for to deploy

   ![image](https://github.com/user-attachments/assets/7b686a1f-1a9b-4ed9-911a-ad848928092b)

   a ) configure  artifacts properties and enable artifact trigger

    ![image](https://github.com/user-attachments/assets/dadcfaee-e054-4b1f-a8b3-080ce7cfb32c)

  b) configure deployment properties 

  ![image](https://github.com/user-attachments/assets/9edeb0b0-2b28-44aa-8304-07e62588e4bb)


7. go to azure artifacts promote to Pre release from local , so that release piepline gets triggered

   ![image](https://github.com/user-attachments/assets/573895c4-2e0b-4e99-aa5c-36dd6d34d0b4)


8. deploy started after trigger from artifacts

   ![image](https://github.com/user-attachments/assets/d4b4129c-b03f-4012-a192-439cd226f320)


9. deployment successfull

    ![image](https://github.com/user-attachments/assets/4fb428f7-baeb-4bb0-9f92-16a74fc13ea8)


 view app on 

 ![image](https://github.com/user-attachments/assets/75f8c2d4-94e7-4fae-b921-efd3cc55dd39)

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


3. give permissions to artifact components created earlier

   ![image](https://github.com/user-attachments/assets/fe568c1c-4b40-4f30-ad16-7c223145f481)


4.

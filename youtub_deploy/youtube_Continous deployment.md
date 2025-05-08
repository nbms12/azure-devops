I have achieved  making automated relaease of youtube application into staging(Dev ) and Prod environments , respectively 

req services : 
  1. two app services for staging(Dev ) and Prod environments.
  2. create two deployment slots



1. create a pipline upto build stage, once build is complete it can generate artifacts for next steps 

![image](https://github.com/user-attachments/assets/2a8f0eb9-703a-4862-b390-8258a75e7122)


2.create a new release and upoad artifacts in artifact stage, ( meanning artifacts must be ready if build success ) 
![image](https://github.com/user-attachments/assets/5078a3c0-7dd3-45db-939b-ce302b34fdc6)


3. enable trigger option for Contrinous Deployment ( CD ) from main branch.

   ![image](https://github.com/user-attachments/assets/2577abe0-56a6-4187-add3-57798446b0c4)


4.

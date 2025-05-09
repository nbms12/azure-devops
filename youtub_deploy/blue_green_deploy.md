continued from prevoius project , i started blue- green deployment using azure devops with 2 pipelines allocated, below is my strategy
to acheive this 

![image](https://github.com/user-attachments/assets/7136d487-cd07-4a8a-ba35-8012bd79d8f6)


1. create 2 different pipelines , with attached to main and release branches resprctively.

   ![image](https://github.com/user-attachments/assets/3c3f8197-ef99-4f5e-86ac-2c71e20f667d)

2.publish artifacts from each of the pipeline and be ready for next steps 

3. edit release pipeline , add new artifact stage and deploy stage ( below diagram )

   ![image](https://github.com/user-attachments/assets/21c88666-ddc6-4ce5-971d-cfdbb4544563)

4. configure artifact stage for Green Deploy

   ![image](https://github.com/user-attachments/assets/1cd5f5dd-b4a0-4c60-9a68-9a05ccace45e)

5. enable trigge point from release branch only

   ![image](https://github.com/user-attachments/assets/591d4056-1ba8-48a7-bab4-b81d4b7498a6)
   
6. configure Green deploy stage ( select slot by name newfeature MANDATORY )

   ![image](https://github.com/user-attachments/assets/d9619757-a3a0-4048-99df-55eb18d0d8d7)

7. make pre - deployment conditions are SELF- APPROVERS

8. release pipelines are triggered once artifacts published succesfully

   ![image](https://github.com/user-attachments/assets/423521e6-8fc0-49d6-8d9e-52c9352d02dd)


9.check logs for prod - server deploy , we can see app is deployed into main server ( live ) 
![image](https://github.com/user-attachments/assets/b11b7b4e-4a87-4286-9cd7-38af7846b1a8)

10.check logs for  new feature server 

11. Prod -server app ( LIVE )  BLUE - DEPLOY 

    ![image](https://github.com/user-attachments/assets/3841a377-1542-4937-b468-3ec3c970bb0c)


12. New feature - Green deploy , as we can see and verify that sidebar Icons  color is changed to Blue instead of Red  ( as NEW Feature )

![image](https://github.com/user-attachments/assets/5e5412d7-6df2-497c-8135-2470673d2dfe)



Once its approved we can swap from green to Blue deployment , so that we can new feature in LIVE .

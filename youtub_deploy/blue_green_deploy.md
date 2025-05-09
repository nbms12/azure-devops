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
   
6. configure Green deploy stage ( select slot by name feature MANDATORY )

   ![image](https://github.com/user-attachments/assets/d9619757-a3a0-4048-99df-55eb18d0d8d7)

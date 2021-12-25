Campaign Response Model
------------------------------------------------------------------

หัวข้อนี้เป็นการศึกษาการตอบสนองของลูกค้าต่อแคมเปญสินค้า โดยนำไฟล์ Retail_Data_Response และ Retail_Data_Transactions มา Predict การตอบสนองของลูกค้าต่อแคมเปญสินค้า

![image](https://user-images.githubusercontent.com/82756975/147391290-b2f012cc-fedd-467b-be57-142925484078.png)
![image](https://user-images.githubusercontent.com/82756975/147391234-3925480e-f937-4c4b-9bad-7c55d6455714.png)
![image](https://user-images.githubusercontent.com/82756975/147391318-5b2f87d5-46db-4986-95dd-546713f68c14.png)
![image](https://user-images.githubusercontent.com/82756975/147391328-384029c7-d2a4-4cd3-88ec-55f5a92091eb.png)

จาก Data พบว่า Output มีความ Imbalance สูง จึงใช้วิธี SMOTE แก้ไขให้ดีขึ้น
![image](https://user-images.githubusercontent.com/82756975/147391274-c9452362-9ac1-42d4-84ed-2597c9351260.png)

Model ที่เราจะใช้ในการ Train และ Test Data ได้แก่ Logistic Regression, XGBoost, CatBoost Classifier 

![image](https://user-images.githubusercontent.com/82756975/147391382-a0ac2261-b237-42fd-b09f-e1b076312a17.png)
Model ที่มีความ Accuracy มากที่สุด คือ 'CatBoost model - SMOTE CLV' เท่ากับ 0.83 (Training Set) และ 0.70 (Testing Set)

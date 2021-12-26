# CUSTOMER SEGMENTATION
-------------------------------------------------------
เป็นการศึกษาเพื่อแบ่งกลุ่มลูกค้าจากพฤติกรรมที่คล้ายหรือเหมือนกันในการเลือกซื้อสินค้าหรือบริการ โดยตัวอย่างต่อไปนี้เป็นข้อมูลลูกค้าจากไฟล์ Supermarket Data.csv เหมือนกับหัวข้อ 01-CLV-Dashboard จะใช้วิธี K-Mean ในการจำแนกลูกค้าเป็นกลุ่ม

![image](https://user-images.githubusercontent.com/82756975/147416086-d2c26dbc-9ec4-46d0-9af0-b2ce9d840afa.png)

![image](https://user-images.githubusercontent.com/82756975/146320746-a8f67016-e13b-42ac-955b-4ca96b95c7da.png)

![image](https://user-images.githubusercontent.com/82756975/146320782-ac3f8239-501f-4bb3-a985-93fcdb829261.png)

![image](https://user-images.githubusercontent.com/82756975/146320830-e92b42a8-f926-4847-a5ed-cab03947b6da.png)

![image](https://user-images.githubusercontent.com/82756975/146320682-81a7242e-d881-4899-b392-af89c0231167.png)

Interpret results and plan for actions
1. Define features โดย Calculate Feature ได้แก่ TotalSpend, TotalVisits, TotalSKUs, FirstDate, LastDate, TicketSize, total_days, recency ก่อนทำสร้าง Model
2. ทำการ fit model K-mean ได้คอลัมน์ที่บ่งบอกถึงการแบ่งกลุ่ม Cluster 0,1,2,3
3. ทำ Feature Importance โดย DecisionTreeClassifier เพื่อหาความสำคัญของ Feature แต่ละตัว
4. plan for action โดยดูแต่ละ Cluster แบ่งลูกค้าใน Cluster ตาม CUST_LIFESTAGE, PROD_CODE ตามลำดับ เพื่อจัดอันดับสินค้าที่มีการซื้อสูงที่สุด TotalSpend > 1,000,000 Bahts
5. ทำการ Product Recommendation สินค้านั้นๆ ให้แต่ละกลุ่ม Lifestage เพื่อให้ตรงกับความต้องการมากที่สุด ผ่าน Social Media โดยอาจแจกคูปองส่วนลด, ของแถม เป็นต้น

#CLV Dashboard
----------------------------------------------------------------------
หัวข้อนี้จะเป็นการนำข้อมูลในไฟล์ Supermarket Data.csv ในเว็บไซต์ https://www.dunnhumby.com มาทำการศึกษาเพื่อหา CLV Insight ของ Supermaket
![pexels-andrea-piacquadio-3796810](https://user-images.githubusercontent.com/82756975/146158076-097c84bf-f46e-4c95-8b80-335dd058d6ca.jpg)

เรามาเริ่มกันที่ตาราง Summary
![summary_table](https://user-images.githubusercontent.com/82756975/146159343-2ba8ac79-e441-44ee-acf8-264301ec9543.jpg)

โดยรายงานผลผ่าน Feature ใหม่ ได้แก่ ACTIVE MEMBER, COUNT_BASKET, CUST_PER_BASKET, TICKET SIZE, ARPU, CHURN, ALT, CLV, TRANS_PER_MONTH

- ACTIVE MEMBER = DISTINCTCOUNT(CUST_CODE)
- COUNT_BASKET = DISTINCTCOUNT(BASKET_ID)
- CUST_PER_BASKET = ACTIVE_MEMBER / COUNT_BASKET
- TICKET SIZE = Total SPEND / BASKET_ID
- ARPU = total SPEND / DISTINCTCOUNT(CUST_CODE)
- CHURN = active member previous month - ACTIVE MEMBER / active member previous month
- ALT = 1 / CHURN
- CLV = ARPU * 0.1 * ALT
- TRANS_PER_MONTH = Total BASKET_ID / month

![insight_store](https://user-images.githubusercontent.com/82756975/146161339-add5db3c-810d-4478-b5ee-3e9d3d39074c.jpg)


![SPEND_CLV](https://user-images.githubusercontent.com/82756975/146161378-9ce2b6b5-188f-4e34-bb19-ce957a4e171a.jpg)


![ticket_size](https://user-images.githubusercontent.com/82756975/146161389-7412e040-0348-44d2-b6f6-d21def144fa8.jpg)


![prod_code_40](https://user-images.githubusercontent.com/82756975/146161401-5f12aa37-72da-4845-882a-50966cb2135b.jpg)

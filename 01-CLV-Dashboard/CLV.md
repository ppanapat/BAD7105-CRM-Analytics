# CLV Dashboard
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

จากกราฟข้างต้น
- TRANS_PER_MONTH by Year and STORE_CODE แสดงจำนวน transaction ของร้านค้าที่ 1 และ 2 ที่เกิดขึ้นในแต่ละปี (ปี 2006-2008)
- ACTIVE_NUMBER by YEAR and STORE_CODE แสดงจำนวนลูกค้าที่มาซื้อสินค้าในร้านค้าที่ 1 และ 2 ในแต่ละปี (ปี 2006-2008)
- TOTAL_SPEND by SHOP_HOUR and STORE_CODE แสดงยอดการซื้อสินค้าเทียบกับเวลาแต่ละชั่วโมงและสาขาร้านค้า
- Count of BASKET_DOMINANT_MISSION by STORE_CODE and BASKET_DOMINANT_MISSION แสดงปริมาณสินค้าแต่ละประเภทที่ลูกค้าซื้อในแต่ละสาขา
- TOTAL_SPEND by CUST_LIFESTAGE แสดงยอดใช้จ่ายทั้งหมดเทียบกับลูกค้าแต่ละวัย
- TOTAL_SPEND by SHOP_HOUR and CUST_LIFESTAGE แสดงยอดใช้จ่ายทั้งหมดเทียบกับเวลาแต่ละชั่วโมงและลูกค้าแต่ละวัย

![SPEND_CLV](https://user-images.githubusercontent.com/82756975/146161378-9ce2b6b5-188f-4e34-bb19-ce957a4e171a.jpg)

จากกราฟข้างต้น
- SPEND by DATE แสดงยอดการซื้อแต่ละวัน
- ACTIVE_NUMBER by DATE แสดงจำนวนลูกค้าแต่ละวัน
- TOTAL_SPEND by PROD_CODE_40 แสดงยอดการซื้อทั้งหมดจำแนกเป็นแต่ละชนิดสินค้า CODE 40
- Count of PROD_CODE_40 by SHOP_HOUR and PROD_CODE_40 แสดงจำนวนสินค้าแต่ละชนิด CODE 40 เทียบกับเวลาแต่ละชั่วโมง
- CLV by Year แสดงค่า CLV แต่ละปี (ปี 2006-2008)

![ticket_size](https://user-images.githubusercontent.com/82756975/146161389-7412e040-0348-44d2-b6f6-d21def144fa8.jpg)


![prod_code_40](https://user-images.githubusercontent.com/82756975/146161401-5f12aa37-72da-4845-882a-50966cb2135b.jpg)

Scatter Plot ข้างต้น แสดงสินค้าแต่ละชนิด CODE 40 ที่อยู่ในแต่ละตะกร้า มีปริมาณที่ถูกซื้อเท่าไหร่ และยอดการซื้อเท่าไหร่ในตะกร้า

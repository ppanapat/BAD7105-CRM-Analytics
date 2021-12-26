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

พบว่า
- สาขาที่ 1 มีรายการซื้อสินค้ามากกว่า สาขา 2 ในช่วงปี 2006-2008
- สาขาที่ 1 มีลูกค้ามาซื้อสินค้ามากกว่า สาขา 2 ในช่วงปี 2006-2008
- ช่วงเวลา 13.00-15.00 น. และ 21.00 น. เป็นต้นไป ร้านค้าสามารถขายสินค้าได้มากที่สุด
- สินค้าที่ลูกค้าซื้อมากที่สุด 3 อันดับ ได้แก่ Fresh, Mixed และ Grocery ตามลำดับ
- 3 อันดับของช่วงอายุที่มียอดซื้อสินค้ามากที่สุด ได้แก่ OT, YF และ OA ตามลำดับ (และทุกเวลาชั่วโมง)

![SPEND_CLV](https://user-images.githubusercontent.com/82756975/146161378-9ce2b6b5-188f-4e34-bb19-ce957a4e171a.jpg)

จากกราฟข้างต้น
- SPEND by DATE แสดงยอดการซื้อแต่ละวัน
- ACTIVE_NUMBER by DATE แสดงจำนวนลูกค้าแต่ละวัน
- TOTAL_SPEND by PROD_CODE_40 แสดงยอดการซื้อทั้งหมดจำแนกเป็นแต่ละชนิดสินค้า CODE 40
- Count of PROD_CODE_40 by SHOP_HOUR and PROD_CODE_40 แสดงจำนวนสินค้าแต่ละชนิด CODE 40 เทียบกับเวลาแต่ละชั่วโมง
- CLV by Year แสดงค่า CLV แต่ละปี (ปี 2006-2008)

พบว่า
- ยอดซื้อสินค้าช่วงสิ้นปีมีค่ามากอย่างมีนัยสำคัญ อาจมีปัจจัยต่างๆ ที่มีผลต่อการซื้อสินค้าของลูกค้า เช่น การล้างสต๊อกสินค้า โบนัสของพนักงานบริษัทฯ เป็นต้น
- ยอดซื้อสินค้าในช่วงเดือนมกราคมมีค่าน้อยลงจากเดือนธันวาคมมาก อาจเป็นเพราะการกักตุนสินค้าของลูกค้ามาตั้งแต่ปลายปีที่ผ่านมา สินค้ามีการเปลี่ยนแปลงราคาหรือคุณภาพ หรือร้านค้าเปลี่ยนสินค้าที่วางขาย เป็นต้น
- ลูกค้าที่เป็นสมาชิกมาซื้อสินค้าทุกเดือนใกล้เคียงกัน สะท้อนความสามารถในการดึงลูกค้าให้มาซื้อสินค้าได้ทุกช่วงเวลา และมากที่สุดในช่วงธันวาคม อาจเพราะมีโปรโมชั่นสำหรับสมาชิก หรือแต้มสมาชิกใกล้หมดอายุ จึงต้องรีบใช้ เป็นต้น แต่ในช่วงมกราคมลูกค้ามาซื้อน้อยลง อาจเกิดจากเหตุผลเดียวกับข้อข้างต้น
- สินค้า CODE 40 ที่มียอดซื้อมากที่สุด 5 อันดับ ได้แก่ D00002, D00003, D00008, D00005 และ D00001 ตามลำดับ

![ticket_size](https://user-images.githubusercontent.com/82756975/146161389-7412e040-0348-44d2-b6f6-d21def144fa8.jpg)


![prod_code_40](https://user-images.githubusercontent.com/82756975/146161401-5f12aa37-72da-4845-882a-50966cb2135b.jpg)

Scatter Plot ข้างต้น แสดงสินค้าแต่ละชนิด CODE 40 ที่อยู่ในแต่ละตะกร้า มีปริมาณที่ถูกซื้อเท่าไหร่ และยอดการซื้อเท่าไหร่ในตะกร้า

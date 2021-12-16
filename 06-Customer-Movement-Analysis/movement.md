Customer Movement Analysis
----------------------------------------------------------------
![churn customer](https://user-images.githubusercontent.com/82756975/146315859-be8a05b9-b8e8-4e09-b698-97db7d3c49eb.jpg)

เป็นการวิเคราะห์เพื่อหาการเคลื่อนไหวของลูกค้าว่า ในแต่ละช่วงเวลา มีลูกค้าใหม่ (New Customer), ลูกค้าเดิมกลับมาซื้อสินค้า (Reactivate Customer), ลูกค้าซื้อประจำ (Repeat Customer) และลูกค้าที่บอกเลิกแล้ว (Churn Customer) เป็นสัดส่วนเท่าไหร่ หรือจำนวนเท่าไหร่


โดยการวิเคราะห์ครั้งนี้ ผมได้ใช้ไฟล์ Supermaket Data.csv จากเว็บไซต์ https://www.dunnhumby.com และใช้เครื่องมือใน https://datastudio.google.com/ เพื่อวิเคราะห์ data จากโค้ด SQL และสร้าง Dashboard
ข้อมูลที่จะใช้เป็นช่วงเวลาตั้งแต่ เม.ย.2006-ก.ค.2008
![image](https://user-images.githubusercontent.com/82756975/146314958-7d7cf430-35f9-4187-a052-7b623b3c2d78.png)


![image](https://user-images.githubusercontent.com/82756975/146315016-e8b20551-c29f-420d-9385-bfc28b0fdc7a.png)
![image](https://user-images.githubusercontent.com/82756975/146315051-931dd91d-e09d-43a0-906d-253beae31131.png)


![image](https://user-images.githubusercontent.com/82756975/146315083-3be36513-ce2b-47bf-bdc6-d1199c7c0f7f.png)


![image](https://user-images.githubusercontent.com/82756975/146315107-9051694d-bb78-4e91-be38-7c438eb0ca3d.png)


สรุปได้ว่า
- เริ่มต้นจากเดือน เม.ย. 2006 มี New Customer จำนวน 1,003 คน หลังจากนั้นมี New Customer ทุกเดือนแต่ลดลงเรื่อยๆจนถึง เม.ย.2008 ที่ไม่มี New Customer
- Repeat Customer มีอัตราส่วนที่ Steady แสดงว่า ร้านค้ามีการจัดการรักษาลูกค้าให้กลับมาซื้อเป็นประจำได้ดี อาจจะเป็นเรื่องทำเลที่ตั้ง ราคาสินค้า หรือแคมเปญ
- Reactivated Customer มีสัดส่วนที่เพิ่มขึ้น แสดงให้เห็นว่า ร้านค้ามีการใช้แคมเปญ หรือการประชาสัมพันธ์อื่นๆ เพื่อดึงลูกค้าที่ไม่ค่อยได้ซื้อสินค้า กลับมาซื้อได้ดี
- Churn Customer มีทุกช่วงเวลา แต่มีอัตราส่วนที่ยังน้อย เมื่อเทียบกับ New Customer + Repeat Customer + Reactivated Customer ยกเว้นเดือนสุดท้าย
- เดือน ก.ค. 2008 มีเหตุการณ์บางอย่างเกิดขึ้น ทำให้ไม่มี New Customer ส่วน Repeat Customer + Reactivated Customer ลดลงมาก และไปเพิ่มขึ้นในส่วนของ Churn Customer สะท้อนว่า กิจการอาจประสบปัญหา หรืออาจเลิกกิจการในช่วงเวลาถัดไป ซึ่งหากประสบปัญหาควรรีบแก้ไขเพื่อรักษาฐานลูกค้า

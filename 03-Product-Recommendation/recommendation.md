Product Recommendation
------------------------------------------------------
เป็นการวิเคราะห์สินค้าที่ลูกค้าซื้อว่า หากซื้อสินค้าหลายชนิดในตะกร้าเดียวกัน จะมีความสัมพันธ์กันในตัวสินค้าแต่ละชนิดมั้ย หากมีความสัมพันธ์กันมาก ก็จะนำมาแนะนำให้ลูกค้าซื้อคู่กัน อาจจะเริ่มจากวางสินค้าบนแผงใกล้กัน โปรโมชั่นซื้อคู่กันแล้วลดราคา หรือการนำเสนอบนโซเชี่ยลมีเดีย เพื่อช่วยให้จำหน่ายสินค้าให้ได้มากขึ้น และตรงกับความต้องการของลูกค้า


![istockphoto-904231604-612x612](https://user-images.githubusercontent.com/82756975/146310499-a5828fbc-6a49-4619-922b-c02b907043e0.jpg)



ตัววัดประสิทธิภาพที่น่าสนใจ ได้แก่

Support คือตัววัดประสิทธิภาพในการซื้อสินค้าชนิดนั้นในตะกร้าเทียบกับจำนวนสินค้าในตะกร้าทั้งหมด P(A), P(B)

Confidence เป็นตัววัดประสิทธิภาพความมั่นใจในการซื้อสินค้าตั้งแต่ 2 ชนิดขึ้นไป เพื่อดูความน่าจะเป็นเมื่อซื้อสินค้า A แล้วจะซื้อสินค้า B ด้วย (P(A/B)) โดยนำตะกร้าที่ทั้ง A และ B เทียบกับตะกร้าที่มี A

Lift เป็นตัววัดประสิทธิภาพสำหรับ association rule ที่ทำการเปรียบเทียบ ความน่าจะเป็นที่จะพบสินค้า A ในตะกร้าที่มี B เทียบกับความน่าจะเป็นที่จะพบสินค้า A (Confidence/Lift) => P(A และ B)/P(A)*P(B)




โดย dataset ที่นำมาใช้ เป็นผลสำรวจจากนักศึกษาใน Class วิชา Customer Relationship Management ของคณะสถิติประยุกต์ NIDA ทั้งหมด 46 คน โดยให้นักศึกษาเลือกสินค้าตัวอย่างที่จะซื้อคนละ 1 อย่าง และทำการโหวตกันว่า มีใครเลือกซื้อสินค้าอะไรใส่ในตะกร้าบ้าง


![Screenshot 2021-12-16 115146](https://user-images.githubusercontent.com/82756975/146310373-e0a8c1c5-ccac-496c-9e89-002e860031fa.jpg)


Interpret results and plan for actions
สินค้าที่สนใจ ได้แก่

Item 1 คือ Salmon Sashimi, พลาสเตอร์บรรเทาปวด ตราเสือ

Item 2 คือ ยาดม

อาจทำโปรโมชั่น ซื้อคู่กันระหว่าง Salmon Sashimi-ยาดม และ พลาสเตอร์บรรเทาปวด ตราเสือ-ยาดม

antecedent support P(Item 1) = 0.5

consequent support P(Item 2) = 0.825

support = 0.5

confidence P(A|B)= 1

lift = 1.21 แปลว่า Surprise ที่สินค้า 2 อย่างจะซื้อเหมือนกันสูง

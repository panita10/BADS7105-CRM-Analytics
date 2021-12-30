# Voice of Customer

### Notebook : [Voice of Customer](https://github.com/panita10/BADS7105-CRM-Analytics/blob/main/Assignment07%20-%20Voice%20of%20Customer/Voice_of_Customer.ipynb)
### Colab : [Voice of Customer](https://colab.research.google.com/drive/19G_HzecXMeRX7mJS29LZyeUZrkUKQrYm)

## Dataset

ข้อมูลความคิดเห็นที่มีต่อร้านอาหารและ รีวิวในเว็บไซต์ Wongnai ทั้งหมด 300 รีวิว
![image](https://user-images.githubusercontent.com/92771399/147747022-41dd8938-7255-4ddc-a113-749adc1cb7b7.png)

## Text Preprocessing
### Step 1 - document embedding and dimension reduction
### Step 2 - document clustering using KMeans

![image](https://user-images.githubusercontent.com/92771399/147747107-f824210d-131c-48e5-a008-c01487f7eb86.png)

### Step 3 - document clustering using Agglomorative Clustering with cosine similarity
![image](https://user-images.githubusercontent.com/92771399/147747131-936ea318-6dbf-41d1-a3ec-b173282943dc.png)

### Step 4 - result discussion

Cluster 0 : กลุ่มที่มีจำนวนคำที่เจอเยอะที่สุด 
Cluster 1 : กลุ่มที่มีจำนวนคำที่เจอเยอะเป็นอันดับที่ 2
Cluster 2 : กลุ่มที่มีจำนวนคำที่เจอเยอะเป็นอันดับที่ 3
Cluster 3 : กลุ่มที่มีจำนวนคำที่เจอน้อยที่สุด

## ประเภทร้านของแต่ละ Cluster
Cluster ID 0 : คาเฟ่
ค่าเฟ่ที่มีบรรยากาศดี มีเมนูทั้งเครื่องดื่มและ ขนม ที่อาจจะได้รับรีวิวเยอะๆหรือกำลังเป็นกระแส เนื่องจากมี keyword เกี่ยวกับคำว่า ลอง,ครั้งแรก
Cluster ID 1 : ร้านอาหารไทย/ร้านน้ำผลไม้
น่าจะเป็นร้านอาหารไทยเก่าแก่ ที่อาจจะมีการขายผลไม้หรือเครื่องดื่มจากผลไม้ด้วย รีวิวที่ได้ ค่อนข้างเน้นไปที่อาหารรสชาติดี
Cluster ID 2 : ร้านชานมไข่มุก/เครื่องดื่ม
ร้านชานมไข่มุกที่น่าจะมีหลายสาขา keyword ส่วนใหญ่พูดถึงชาชนิดต่างๆ นม ไข่มุก และอาจจะมีปัญหาเรื่องพนักงาน
Cluster ID 3 : ร้านกาแฟ
ร้านกาแฟ/คาเฟ่ด้านกาแฟโดยเฉพาะ เนื่องจาก keyword ส่วนใหญ่เกี่ยวข้องกับกาแฟ เช่น ร้านกาแฟ กาแฟ สายพันธุ์ เมล็ด



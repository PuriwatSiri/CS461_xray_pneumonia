# CS461_xray_pneumonia
# AI-Powered Pneumonia Detection from Chest X-Rays

```bash
1. สิ่งที่ต้องมี
* Python 3.8+
* Jupyter Notebook / Google Colab

2. ติดตั้ง Libraries
pip install tensorflow numpy matplotlib scikit-learn flask

3.ดาวโหลดไฟล์ Kaggle.json

วิธีการรันโปรเจกต์ (Run Commands)

1. การเทรนโมเดล (Model Training)
หากต้องการเทรนโมเดลใหม่หรือดูผลการวิเคราะห์ข้อมูล:

เปิดไฟล์ Project (1).ipynb ด้วย Jupyter Notebook หรือ Google Colab

รันเซลล์คำสั่งทีละขั้นตอน (Step-by-step execution) ตั้งแต่:

Data Preprocessing: การเตรียมข้อมูลและทำ Augmentation

Baseline Model: การเทรน MobileNetV2

Fine-Tuned Model: การเทรน VGG16 (Model หลัก)

Evaluation: การดูผล Confusion Matrix และกราฟเปรียบเทียบ

2. การเปิดใช้งานระบบ Demo (Web App Deployment)
เราได้เตรียม Web Application อย่างง่ายด้วย Flask เพื่อทดสอบโมเดล:

ตรวจสอบว่ามีไฟล์ pneumonia_vgg16_model.h5 อยู่ในโฟลเดอร์โปรเจกต์

รันคำสั่งต่อไปนี้ใน Terminal:

Bash

python app.py
เมื่อ Server เริ่มทำงาน จะปรากฏลิงก์ (เช่น http://127.0.0.1:5000/)

เปิดลิงก์ดังกล่าวใน Web Browser

การใช้งาน:

คลิกปุ่ม "Choose File" เพื่อเลือกภาพ X-Ray (.jpg/.png)

คลิกปุ่ม "Predict"

ระบบจะแสดงผลวินิจฉัยว่าเป็น NORMAL หรือ PNEUMONIA พร้อมค่าความมั่นใจ

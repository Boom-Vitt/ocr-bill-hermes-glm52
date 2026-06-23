# OCR Bill Manager

เว็บไซต์สำหรับจัดการบิลเงินโดยใช้ OCR (Optical Character Recognition) อ่านตัวอักษรจากรูปบิล/ใบเสร็จและแปลงเป็นข้อมูลที่จัดการได้

## ฟีเจอร์

- อัปโหลดรูปบิลได้ทั้งแบบคลิกและลากวาง (Drag & Drop)
- OCR อ่านตัวอักษรภาษาไทย + อังกฤษ ด้วย Tesseract.js
- แยกข้อมูลสำคัญอัตโนมัติ: วันที่, ผู้ออกบิล, จำนวนเงิน
- ตารางสรุปบิลทั้งหมด พร้อมคำนวณยอดรวม
- Export ข้อมูลเป็น JSON และ CSV
- บันทึกข้อมูลใน LocalStorage (ไม่ต้องมี Backend)
- รองรับ Mobile Responsive

## เทคโนโลยี

- HTML5 + CSS3 + JavaScript (Vanilla)
- [Tesseract.js](https://tesseract.projectnaptha.com/) — OCR Engine ทำงานใน Browser
- GitHub Pages สำหรับ Hosting

## วิธีใช้

1. เปิดเว็บไซต์
2. อัปโหลดรูปบิล/ใบเสร็จ (PNG หรือ JPG)
3. กดปุ่ม "เริ่ม OCR"
4. รอให้ประมวลผลเสร็จ — ข้อมูลจะถูกแยกและบันทึกลงตารางอัตโนมัติ
5. Export เป็น JSON หรือ CSV ได้ตามต้องการ

## สร้างโดย

Hermes Agent (GLM-5.2 via Ollama Cloud)
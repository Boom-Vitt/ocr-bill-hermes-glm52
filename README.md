# OCR Bill Manager

เว็บไซต์สำหรับจัดการบิลเงินโดยใช้ OCR (Optical Character Recognition) อ่านตัวอักษรจากรูปบิล/ใบเสร็จและแปลงเป็นข้อมูลที่จัดการได้

## ฟีเจอร์

- อัปโหลดรูปบิลได้ทั้งแบบคลิกและลากวาง (Drag & Drop)
- OCR อ่านตัวอักษรภาษาไทย + อังกฤษ ด้วย Ollama Vision API หรือ Tesseract.js fallback
- ตั้งค่า Ollama API key/model/endpoint ในหน้าเว็บได้ โดยไม่ hardcode key ลง GitHub Pages
- แยกข้อมูลสำคัญอัตโนมัติ: วันที่, ผู้ออกบิล, จำนวนเงิน
- ตรวจ/แก้ข้อมูลหลัง OCR ก่อนบันทึก ลดปัญหา OCR อ่านผิด
- เพิ่มบิลเองได้แม้ไม่มีรูปหรือ OCR อ่านไม่ครบ
- Dashboard สรุปจำนวนบิล ยอดรวม และค่าเฉลี่ยต่อบิล
- ตารางสรุปบิลทั้งหมด พร้อมคำนวณยอดรวม
- Export ข้อมูลเป็น JSON และ CSV
- บันทึกข้อมูลใน LocalStorage (ไม่ต้องมี Backend)
- รองรับ Mobile Responsive

## เทคโนโลยี

- HTML5 + CSS3 + JavaScript (Vanilla)
- Ollama Vision API (OpenAI-compatible chat completions) สำหรับ OCR แบบ multimodal
- [Tesseract.js](https://tesseract.projectnaptha.com/) — OCR Engine fallback ทำงานใน Browser
- GitHub Pages สำหรับ Hosting

## วิธีใช้

1. เปิดเว็บไซต์
2. เลือก OCR Engine: Ollama Vision API หรือ Tesseract.js
3. ถ้าใช้ Ollama ให้วาง API key ในช่องตั้งค่า (เก็บเฉพาะ localStorage ของ browser)
4. อัปโหลดรูปบิล/ใบเสร็จ (PNG หรือ JPG)
5. กดปุ่ม "เริ่ม OCR"
6. ตรวจ/แก้ข้อมูลที่ระบบอ่านได้ แล้วกดบันทึก
7. Export เป็น JSON หรือ CSV ได้ตามต้องการ

## สร้างโดย

Hermes Agent (GLM-5.2 via Ollama Cloud)
# 📌 Help desk ticket Management System

## 🔍 เกี่ยวกับโปรเจกต์
โปรเจกต์นี้เป็นโจทย์ข้อสอบสำหรับเข้าคัดเลือกเป็นนักศึกษาฝึกงานของนิภา คือ ระบบจัดการตั๋วสนับสนุน ที่สามารถทำการสร้างตั๋ว ทำการอัปเดตข้อมูลตั๋วและสถานะของตั๋ว สามารถกรองและเรียงข้อมูลตั๋วจากสถานะและวันที่อัปเดต

พัฒนาโดย นางสาวอารดา แว่นวงษ์ ซึ่งมีการพัฒนาระบบตั้งแต่การออกแบบและพัฒนาระบบทั้ง frontend และ backend รวมถึงการจัดการฐานข้อมูล

## 🛠 เทคโนโลยีที่ใช้  
- **Frontend:** React  
- **Backend:** Golang  
- **Database:** PostgreSql  
- **อื่น ๆ:** Docker

## 🚀 วิธีติดตั้งและใช้งาน 
#### 1. การติดตั้งและการใช้งาน Database
- ทำการ get database จาก https://github.com/arada1110/ticketdatabase ด้วยคำสั่ง git clone
```bash
# เปิด command prompt or terminal บนระบบปฏิบัติการของเครื่อง
git clone https://github.com/arada110/ticketdatabase

cd ticketdatabase
```
- จากนั้นทำการ run docker เพื่อสร้าง environment ของ database บนเครื่องของเรา
```bash
# คำสั่งรัน docker
docker-compose up -d
```
- จะเปิด URL: http://localhost:5050 เพื่อเปิด pgAdmin สำหรับจัดการฐานข้อมูล
- เข้าใช้งาน pgAdmin จาก environment ที่กำหนดไว้ในไฟล์ .env

#### 2. การติดตั้งและการใช้งาน Service API
- ทำการ get service จาก https://github.com/arada1110/ticketapi ด้วยคำสั่ง git clone
```bash
git clone https://github.com/arada110/ticketapi

cd ticketapi
```
- จากนั้นไปที่ไฟล์ .env เพื่อทำการตั้งค่า environment ของเครื่อง เพื่อทำการเปลี่ยนหมายเลข IPv4 ให้เป็นของเครื่องที่ใช้งานอยู่
```bash
# เปิด terminal or command prompt ใช้คำสั่งนี้หาหมายเลข IPv4
ipconfig

# ทำการแก้ไข
DB_HOST=แทนด้วยหมายเลข IP ที่หามาจาก ipconfig
```
- ทำการรัน docker
```bash
# คำสั่งรัน docker
docker-compose build

docker-compose up -d
```
- จะเปิด URL: http://localhost:8080 สำหรับเรียกดูข้อมูลผ่านการทำ api

#### 3. การติดตั้งและการใช้งานหน้าเว็บ Help desk ticket
- ทำการ get หน้าเว็บจาก https://github.com/arada1110/helpdesk-ticket-app ด้วยคำสั่ง git clone
```bash
git clone https://github.com/arada1110/helpdesk-ticket-app

cd helpdesk-ticket-app
```
- ทำการติดตั้ง Dependencies ของ React
```bash
# ถ้าใช้ npm
npm install

# ถ้าใช้ yarn
yarn install
```
- จากนั้นทำการรันโปรเจกต์
```bash
# ถ้าใช้ npm
npm start

# ถ้าใช้ yarn
yarn start
```
- จะเปิด URL: http://localhost:3000 สำหรับเรียกดูระบบจัดการตั๋วสนับสนุน

[🎥 ดูวิดีโอสาธิต](https://drive.google.com/file/d/1ldukxlQfbktgXdAgbp8_XabBG2rvGppo/view?usp=sharing)

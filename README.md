# Lab 9: Spring Boot Transaction

REST API สำหรับทดลองการฝากเงินและการ rollback ด้วย Spring Boot, JPA และ PostgreSQL

## เตรียมฐานข้อมูล

```sql
CREATE DATABASE lab9;
```

แก้ `DB_PASSWORD` ให้ตรงกับรหัสผ่าน PostgreSQL หรือแก้ค่าใน `src/main/resources/application.properties`

## รันโปรเจกต์

```powershell
mvn spring-boot:run
```

เซิร์ฟเวอร์ทำงานที่ `http://localhost:8080`

## API

- `POST /accounts` สร้างบัญชี
- `GET /accounts/{id}` ดูบัญชี
- `POST /accounts/{id}/deposit` ฝากเงิน โดยส่ง body เช่น `{ "amount": 1000 }`

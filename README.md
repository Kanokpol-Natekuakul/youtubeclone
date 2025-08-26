# YouTube Clone

โปรเจค YouTube Clone ที่สร้างด้วย React + Vite เพื่อจำลองการทำงานของเว็บไซต์ YouTube

## 🚀 เทคโนโลยีที่ใช้

- **React 19.1.1** - ไลบรารีสำหรับสร้าง User Interface
- **Vite 7.1.2** - Build Tool และ Development Server
- **React Router DOM 7.8.1** - สำหรับการจัดการ Routing
- **Moment.js 2.30.1** - สำหรับจัดการวันที่และเวลา
- **ESLint** - สำหรับตรวจสอบคุณภาพโค้ด

## 📋 ข้อกำหนดของระบบ

- Node.js เวอร์ชัน 18 หรือสูงกว่า
- npm หรือ yarn

## 🛠️ การติดตั้ง

1. **Clone โปรเจค**
   ```bash
   git clone <repository-url>
   cd youtube_clone
   ```

2. **ติดตั้ง Dependencies**
   ```bash
   npm install
   ```

## 🚀 การรันโปรเจค

### Development Mode
```bash
npm run dev
```
เปิดเบราว์เซอร์ที่ `http://localhost:5173`

### Build สำหรับ Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

### ตรวจสอบโค้ดด้วย ESLint
```bash
npm run lint
```

## 📁 โครงสร้างโปรเจค

```
youtube_clone/
├── public/
│   └── vite.svg
├── src/
│   ├── data.js          # ไฟล์ API Key และ utility functions
│   └── (ไฟล์ React components และ assets อื่นๆ)
├── .gitignore
├── eslint.config.js
├── package.json
├── README.md
└── vite.config.js
```

## ⚙️ การตั้งค่า API และ Utility Functions

โปรเจคใช้ไฟล์ `src/data.js` เพื่อเก็บ API Key และ utility functions:

### ตัวอย่างเนื้อหาในไฟล์ `src/data.js`:
```javascript
// API Key สำหรับเชื่อมต่อ YouTube Data API
export const API_KEY = "your_youtube_api_key_here";

// Function สำหรับแปลงตัวเลขให้อยู่ในรูปแบบที่อ่านง่าย (เช่น 1M, 1K)
export const value_converter = (value) => {
    if (value >= 1000000) {
        return (value / 1000000).toFixed(1).replace(/\.0$/, '') + "M";
    } else if (value >= 1000) {
        return (value / 1000).toFixed(1).replace(/\.0$/, '') + "K";
    } else {
        return value.toString();
    }
};
```

### วิธีการใช้งาน:
```javascript
import { API_KEY, value_converter } from './data.js';

// ใช้ value_converter สำหรับแสดงจำนวนการดู
console.log(value_converter(1234567)); // ผลลัพธ์: "1.2M"
console.log(value_converter(12345));   // ผลลัพธ์: "12.3K"
console.log(value_converter(123));     // ผลลัพธ์: "123"
```

## 📝 หมายเหตุสำคัญ

- ไฟล์ `src/data.js` ถูกกำหนดให้ ignore ใน `.gitignore` เนื่องจากมี API Key ที่ไม่ควร commit ขึ้น repository
- **สำคัญ**: อย่าลืมสร้างไฟล์ `src/data.js` และใส่ API Key ของคุณเองก่อนรันโปรเจค
- โปรเจคใช้ ESLint configuration ที่รองรับ React และ JSX
- รองรับ Hot Module Replacement (HMR) สำหรับการพัฒนาที่รวดเร็ว

## 🔧 การปรับแต่ง ESLint

หากคุณต้องการพัฒนาแอปพลิเคชันสำหรับ production และต้องการใช้ TypeScript พร้อมกับ type-aware lint rules ให้ดูข้อมูลเพิ่มเติมที่:
- [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts)
- [typescript-eslint](https://typescript-eslint.io)

## 📄 ข้อมูลเพิ่มเติม

โปรเจคนี้ใช้ template พื้นฐานของ React + Vite ที่มี:
- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) - ใช้ Babel สำหรับ Fast Refresh
- ESLint rules สำหรับการพัฒนาที่มีคุณภาพ

# credit

- https://youtu.be/lpx2zFkapIk?si=X6J7cSRYUhdDVFjb

ฝึกฝนและศึกษาจากคลิปนี้


สร้างด้วย ❤️ โดยใช้ React และ Vite

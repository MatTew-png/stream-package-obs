# 🎮 MatthewDrake - Ultimate Stream Package (OBS Setup Guide)

แพ็กเกจสตรีมนี้ถูกปรับแต่งและแยกโครงสร้างให้สมบูรณ์แบบ 100% พร้อมใช้งานกับ **OBS Studio** (ความละเอียด 1920x1080 Full HD) โดยไม่มีปัญหาภาพเบี้ยวหรือล้นจอ

---

## 📂 1. รายชื่อไฟล์ทั้งหมด และ "อันไหนใช้ตอนไหน?"

### 🎬 หมวดที่ 1: ฉากสตรีมสำเร็จรูป (5 Master Scenes - ใช้งานง่ายที่สุด)
> **วิธีใช้:** ใน OBS สร้าง Scene ขึ้นมา 5 ซีน แล้วเพิ่ม Browser Source เลือกไฟล์ตามแต่ละฉากได้เลย

| ไฟล์ฉาก | ชื่อฉากใน OBS | ⏰ ใช้ตอนไหน? | องค์ประกอบในฉาก |
|---|---|---|---|
| [`Scene_1_Starting_Soon.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/Scene_1_Starting_Soon.html) | **Starting Soon** | **ก่อนเริ่มสตรีม** (เปิดทิ้งไว้ 5-10 นาทีก่อนเปิดไมค์/เปิดเกม ให้คนดูทยอยเข้ามา) | แอนิเมชันเปิดสตรีม, ป้าย STARTING SOON, ลายน้ำคันจิ `まもなく開始`, คริสตัล 3D, ประกายไฟ |
| [`Scene_2_Just_Chatting.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/Scene_2_Just_Chatting.html) | **Just Chatting** | **ตอนนั่งคุยกับคนดู / ปิดเกม / Q&A** | กรอบกล้อง Cam 16:9 + กรอบ Live Chat (เว้นช่องโปร่งใสสำหรับวางกล้องและแชท), ลายน้ำ `雑談配信中` |
| [`Scene_3_Be_Right_Back.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/Scene_3_Be_Right_Back.html) | **Be Right Back (BRB)** | **ตอนลุกไปพัก / เข้าห้องน้ำ / กินน้ำ** (พักเบรกระหว่างสตรีม) | ข้อความ BE RIGHT BACK, ป้าย `AFK / BRB`, ลายน้ำ `一時休憩中` |
| [`Scene_4_Stream_Ending.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/Scene_4_Stream_Ending.html) | **Stream Ending** | **ตอนสตรีมเสร็จ / ขอบคุณคนดู** (เปิดก่อนกดปุ่ม End Stream) | ข้อความ THANKS FOR WATCHING, ป้าย `OFFLINE`, ลายน้ำ `配信終了` |
| [`Scene_5_Gameplay_Overlay.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/Scene_5_Gameplay_Overlay.html) | **In-Game Overlay** | **ตอนกำลังเล่นเกม (FiveM / เกมอื่นๆ)** | พื้นหลังโปร่งใสทั้งจอ 100% มีเพียงโลโก้ MATTHEWDRAKE มุมบน, แถบ Discord, กรอบกล้องมุมจอ |

---

### 🧩 หมวดที่ 2: เลเยอร์โปร่งใสแยกชิ้น (สำหรับคนที่ต้องการ Custom จัดวางเอง)
| ไฟล์เลเยอร์ | รายละเอียด |
|---|---|
| [`01_background_vfx.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/01_background_vfx.html) | เลเยอร์พื้นหลังสีดำ + เลเซอร์สแกน + ประกายไฟ + Manga Speedlines |
| [`02_crystals_and_gifs.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/02_crystals_and_gifs.html) | เลเยอร์คริสตัล 3D 4 มุม + ภาพเคลื่อนไหว Cyber GIFs |
| [`03_header_brand.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/03_header_brand.html) | เลเยอร์โลโก้โปรไฟล์ + ชื่อช่อง MATTHEWDRAKE |
| [`04_center_announcement.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/04_center_announcement.html) | เลเยอร์ข้อความกลางจอ (Starting Soon) |
| [`05_footer_social.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/05_footer_social.html) | เลเยอร์แถบ Discord ด้านล่าง |

---

### 💎 หมวดที่ 3: แบนเนอร์ตกแต่งช่อง
| ไฟล์ | การใช้งาน |
|---|---|
| [`crystal_shard_banners.html`](file:///c:/Users/_newgen/Documents/antigravity/hopeful-mendeleev/crystal_shard_banners.html) | รวมแบนเนอร์ศิลปะคริสตัล 3D ขนาด 1200x134px สำหรับแคปรูปไปแต่งหน้าช่อง Twitch, Kick, YouTube หรือ Discord Banner |

---

## ⚙️ 2. สิ่งที่ต้อง Set ใน OBS ก่อนเริ่มสตรีมจริง (Checklist)

### ✅ จุดที่ 1: การตั้งค่า Browser Source แต่ละอันใน OBS
เมื่อกด `+` เพิ่ม **Browser Source** ใน OBS ให้ตั้งค่าดังนี้:
1. ติ๊กถูก ✅ **Local file** แล้วกด **Browse** เลือกไฟล์ HTML
2. **Width (ความกว้าง):** ใส่ `1920`
3. **Height (ความสูง):** ใส่ `1080`
4. ติ๊กถูก ✅ **Shutdown source when not visible** *(ประหยัด CPU/GPU ขณะไม่ได้เปิดฉากนั้น)*
5. ติ๊กถูก ✅ **Refresh browser when scene becomes active** *(รีเซ็ตเอฟเฟกต์ให้สดใหม่อยู่เสมอ)*

---

### ✅ จุดที่ 2: การเรียงลำดับ Layer ในแต่ละ Scene ของ OBS

#### 🎮 ฉากที่ 1: Just Chatting (พูดคุย)
```text
[บนสุด]  🔼 1. Browser Source (Scene_2_Just_Chatting.html)
        🔼 2. Chat Widget (กล่องแชท เช่น Streamlabs / Botrix)
        🔼 3. Video Capture Device (กล้องเว็บแคม - ปรับขนาดให้พอดีกับช่องกรอบซ้าย)
[ล่างสุด] 🔼 4. Media Source / พื้นหลังสำรอง (ถ้ามี)
```

#### 🕹️ ฉากที่ 2: Gameplay (เล่นเกม FiveM)
```text
[บนสุด]  🔼 1. Browser Source (Scene_5_Gameplay_Overlay.html)
        🔼 2. Video Capture Device (กล้องเว็บแคม วางตรงมุมล่างขวา)
[ล่างสุด] 🔼 3. Game Capture (จับภาพหน้าจอเกม FiveM แบบเต็มจอ 1080p)
```

#### ⏳ ฉากที่ 3: Starting Soon / BRB / Ending
```text
[บนสุด]  🔼 1. Browser Source (Scene_1 / Scene_3 / Scene_4)
        🔼 2. Audio Output Capture (เพลงประกอบสตรีม BGM)
```

---

### ✅ จุดที่ 3: ตั้งปุ่มลัด (Hotkeys) สลับฉากได้ทันทีในคลิกเดียว
ใน OBS ไปที่ **Settings (การตั้งค่า) ➔ Hotkeys (ปุ่มลัด)**:
- **Scene 1 (Starting Soon)** ➔ ตั้งเป็น `Numpad 1` หรือ `F1`
- **Scene 2 (Just Chatting)** ➔ ตั้งเป็น `Numpad 2` หรือ `F2`
- **Scene 3 (Gameplay)** ➔ ตั้งเป็น `Numpad 3` หรือ `F3`
- **Scene 4 (BRB)** ➔ ตั้งเป็น `Numpad 4` หรือ `F4`
- **Scene 5 (Ending)** ➔ ตั้งเป็น `Numpad 5` หรือ `F5`

---

## 📁 ที่อยู่ไฟล์ทั้งหมด (Full Path สำหรับ Copy ไปวาง):
* โฟลเดอร์: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\`
* Scene 1: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\Scene_1_Starting_Soon.html`
* Scene 2: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\Scene_2_Just_Chatting.html`
* Scene 3: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\Scene_3_Be_Right_Back.html`
* Scene 4: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\Scene_4_Stream_Ending.html`
* Scene 5: `C:\Users\_newgen\Documents\antigravity\hopeful-mendeleev\Scene_5_Gameplay_Overlay.html`

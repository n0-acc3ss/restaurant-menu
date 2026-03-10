# 🔔 Silver Bell Restaurant — Online Menu

An elegant, mobile-friendly online menu for **Silver Bell Restaurant** (สโมสรนายทหารอากาศ บางซื่อ), built as a single-file HTML application and deployed via Netlify.

---

## 📋 Project Structure

```
.
├── silverbell-menu.html   # Main menu — single-file app (HTML + CSS + JS)
├── _headers               # Netlify HTTP security headers
├── netlify.toml           # Netlify build & redirect configuration
└── README.md              # This file
```

---

## ✨ Features

- **Category navigation** — all 9 menu categories visible at a glance on first load
- **Search / filter** — live search across Thai and English item names
- **Bilingual** — Thai (default) ↔ English toggle
- **Add to order** — cart flow with running total
- **Special remarks** — one custom note per item (e.g. ไม่เผ็ด / not spicy)
- **เรียกพนักงาน** — call staff button (header + cart)
- **Portion info** — size/weight labels on multi-price items
- **Mobile-first** — fully responsive for phones and tablets
- **No dependencies** — zero npm, zero build step, single `.html` file

---

## 🍽️ Menu Categories

| # | Thai | English |
|---|------|---------|
| 1 | เมนูแนะนำ | Recommended |
| 2 | เมนูกับแกล้ม | Appetizers |
| 3 | เมนูต้มยำ แกงจืด | Tom Yum & Soups |
| 4 | เมนูยำ | Spicy Salads |
| 5 | เมนูแกง / ผัด / ผัดเผ็ด | Stir-fries & Curries |
| 6 | เมนูผัดผัก | Vegetable Stir-fries |
| 7 | เมนูอีสานแซ่บนัว | Isan Menu |
| 8 | เมนูอาหารทะเล | Seafood Menu |
| 9 | เมนูเครื่องดื่ม | Drink Menu |

---

## 🛠️ Updating the Menu

All menu data is stored as a plain JavaScript object inside `silverbell-menu.html`. Search for the `const menuData = {` block near the bottom of the file.

Each item follows this structure:
```js
{ id:'xx00', th:'ชื่อภาษาไทย', en:'English Name', price:'150' }

// For multi-price items, add a portion label:
{ id:'xx00', th:'ชื่อภาษาไทย', en:'English Name', price:'350 / 380', portion:'ราคาตามน้ำหนัก' }
```

To add a new category, add a new `<div class="menu-section">` block in the HTML, a corresponding entry in the `cat-grid` navigation, and a matching key in `menuData`.

---

## 📞 Restaurant Info

| | |
|---|---|
| **Name** | Silver Bell Restaurant |
| **Tel** | 064 569 4482 |
| **Location** | สโมสรนายทหารอากาศ บางซื่อ |
| **Google Maps** | [Open Maps](https://maps.app.goo.gl/JiZZKFzJgRo2KYFt7) |

---

## 📄 License

This project is proprietary. All rights reserved by Silver Bell Restaurant.

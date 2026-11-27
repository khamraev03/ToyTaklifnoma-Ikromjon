# Ikromjon & Dilnura taklifnomasini Render'ga joylash

Bu papka asl taklifnomadan butunlay alohida. Asl saytga (toytaklifnoma.onrender.com) hech narsa tegmaydi.

## 1. GitHub'da yangi repo
1. github.com'da yangi bo'sh repo oching, masalan `ToyTaklifnoma-Ikromjon` (README qo'shmang).
2. Shu papkada (friend-copy) terminal oching va:

```
git init
git add .
git commit -m "Ikromjon & Dilnura taklifnomasi"
git branch -M main
git remote add origin https://github.com/khamraev03/ToyTaklifnoma-Ikromjon.git
git push -u origin main
```

Muhim: asl ToyTaklifnoma papkasida `git add .` qilmang, aks holda friend-copy asl repoga ham tushib qoladi.

## 2. Render'da Web Service
- New + → Web Service → yangi repo'ni tanlang
- Build Command: `npm install`
- Start Command: `node server.js`
- Instance: Free

## 3. Environment Variables (Render → Environment)
- `DATABASE_URL`: yangi Postgres baza yarating, yoki asl saytdagi bazaning URL'ini qo'ying. Ikkinchi holatda ham tilaklar aralashmaydi, chunki bu nusxa `dost_messages` jadvalidan foydalanadi, asl sayt esa `messages` jadvalidan.
- `TABLE_NAME` = `dost_messages`
- `COUPLE_NAMES` = `IKROMJON & DILNURA`
- `BOT_TOKEN`, `CHAT_ID`: ixtiyoriy. Faqat BotFather'dan olingan YANGI bot tokenini qo'ying. Asl saytning tokenini qo'ysangiz, asl saytning Telegram'dagi /delete funksiyasi buziladi. Bo'sh qoldirsangiz, tilaklar baribir saytda saqlanadi, faqat Telegram'ga xabar kelmaydi.
- `PUBLIC_URL`: kerak emas, Render o'zi aniqlaydi.

## 4. Tekshirish
Sayt ochilgach, test tilak yozing: u faqat shu saytda ko'rinishi, asl saytda ko'rinmasligi kerak.

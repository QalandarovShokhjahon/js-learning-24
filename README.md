# 🧠 JavaScript Day 24 — Amaliyot: Loader and Date

Bu darsda men JavaScript’da **Loader va real-time Date/Time** yaratishni amaliyot orqali bajardim.
Bu mashq yordamida DOM, Events, Date Object va setInterval metodlarini birlashtirib ishlashni mustahkamlab oldim.

---

## 🔧 Loyihaning vazifasi / Project Objective

* Foydalanuvchi sahifaga kirganda **loader** ko‘rsatiladi
* Loader bir necha soniyadan keyin yashirinadi
* Sahifada real-time soat ko‘rsatiladi

---

## 📁 HTML tuzilma / Example HTML

```
<div id="loader">Loading...</div>
<div id="content" style="display:none;">
  <h1>Welcome!</h1>
  <p>Current Time: <span id="clock"></span></p>
</div>
```

---

## 💻 JavaScript kodi / JS Code

```
const loader = document.getElementById('loader');
const content = document.getElementById('content');
const clock = document.getElementById('clock');

// Loaderni 3 soniyadan keyin yashirish
setTimeout(() => {
  loader.style.display = 'none';
  content.style.display = 'block';
}, 3000);

// Real-time soat funksiyasi
function updateClock() {
  const now = new Date();
  clock.textContent = now.toLocaleTimeString();
}

setInterval(updateClock, 1000);
```

---

## 🎨 CSS g‘oya / CSS Idea

```
#loader {
  font-size: 24px;
  text-align: center;
  margin-top: 50px;
}

#content {
  text-align: center;
  font-family: Arial, sans-serif;
}
```

---

## 🧩 Qisqacha xulosa / Summary

* `setTimeout()` → loader vaqtincha ko‘rsatish
* `setInterval()` → real-time soat yaratish
* DOM elementlarni `style.display` orqali boshqarish
* Date Object + toLocaleTimeString() bilan vaqtni formatlash

---

## 🎯 Maqsad / Goal

Ushbu amaliyotning maqsadi — JavaScript’da **loader + real-time date** interaktiv elementlarini yaratish va vaqtga asoslangan funksiyalarni qo‘llash.

Buning yordamida:

* Sahifa yuklanish logikasini o‘rganish
* Real-time UI yaratish
* DOM + Date + Timer’larni birgalikda ishlatish
  mumkin bo‘ladi.

---

## 💬 Muallif / Author

✍️ Shokhjahon Qalandarov
📅 Dars: 24-kun — Amaliyot (Loader and Date)

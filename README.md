# Easy-QR Generator
Easy QR Generator is a minimal and fast application for creating QR codes from text or URLs. Built for simplicity, it allows users to generate and download QR codes.

![status](https://img.shields.io/badge/status-active-2ea44f?style=flat-square)
![version](https://img.shields.io/badge/version-1.0.0-fc4955?style=flat-square)
![library](https://img.shields.io/badge/library-qrcodejs-orange?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)

Supports **URL / Text** and **WiFi QR generation**, fully client-side.

---

## Tech stacks

![HTML](https://img.shields.io/badge/HTML5-Structure-E34F26?style=for-the-badge\&logo=html5\&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-Styling-1572B6?style=for-the-badge\&logo=css3\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Logic-F7DF1E?style=for-the-badge\&logo=javascript\&logoColor=black)

---

## Overview

Easy-QR Generator is a single-file HTML + JavaScript widget that generates QR codes in real time.
Powered by `qrcodejs`.

---

## Demo

![Demo](https://img.shields.io/badge/demo-live-blue?style=for-the-badge\&logo=vercel)

👉 https://fersteldev.pl/easy-qr-generator.html

---

## Features

- URL / text QR generation
- WiFi QR generation (WPA / WEP / open network)
- Live QR preview (auto update)
- Mode switching (URL / WiFi)
- Custom QR color picker
- PNG export (download)
- Fully client-side execution

---

## How it works

1. User selects mode (URL or WiFi)
2. Input fields listen for changes (`input` event)
3. Every change triggers `generateQR()`
4. QR is rendered using `QRCode` library

---

## Core functions

### generateQR()

- clears previous QR container
- detects active mode
- builds QR payload
- updates preview link
- renders QR code

**URL mode**
- accepts text or URL
- auto adds `https://` if missing

**WiFi mode**

` WIFI:T:<WPA|WEP|nopass>;S:<SSID>;P:<PASSWORD>;; `

### downloadQR()

Exports QR as PNG.

- detects canvas/image
- converts to dataURL
- creates download link
- saves file as `qr.png`

---

## Events system

```js
document.querySelectorAll("input, select").forEach(el => {
  el.addEventListener("input", generateQR);
});
```
---

## Important

>[!NOTE]
>JavaScript must be enabled for the widget to work.

>[!TIP]
>Library **qrcodejs** must be loaded before initialization.

>[!WARNING]
>WiFi QR compatibility depends on device support.

---

## Dependencies

### qrcodejs

` https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js `

---

## Author

![Author](https://img.shields.io/badge/author-fersteldev-blue?style=for-the-badge)

---

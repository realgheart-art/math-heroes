# Math Heroes — MISI SIFIR (PWA)

App latih tubi matematik yang **boleh dipasang** ke telefon/tablet dan **berfungsi tanpa internet** selepas dibuka kali pertama.

## Isi kandungan pakej
```
index.html               ← aplikasi utama
manifest.json            ← maklumat app (nama, ikon, warna)
sw.js                    ← service worker (mod luar talian)
icon-192.png             ← ikon 192×192
icon-512.png             ← ikon 512×512
icon-maskable-512.png    ← ikon maskable (Android)
apple-touch-icon.png     ← ikon iOS
favicon-32.png           ← ikon tab pelayar
```
> Semua fail **mesti berada dalam folder yang sama**. Jangan ubah nama fail.

## Cara deploy ke GitHub Pages
1. Buat repositori baharu di GitHub (cth: `math-heroes`).
2. Muat naik **kesemua** fail di atas ke root repo (atau drag-and-drop melalui web GitHub).
3. Pergi ke **Settings → Pages**.
4. Di bahagian *Build and deployment*, pilih **Source: Deploy from a branch**, **Branch: main**, folder **/(root)**, kemudian **Save**.
5. Tunggu 1–2 minit. Pautan app akan muncul, cth:
   `https://NAMA-ANDA.github.io/math-heroes/`

> Path dalam pakej ini **relatif** (`./`), jadi ia berfungsi walaupun dalam subfolder repo GitHub Pages. Tiada perubahan kod diperlukan.

## Cara murid pasang ke skrin utama
- **Android (Chrome):** buka pautan → ketik butang **"📲 Pasang Math Heroes…"** dalam app, atau menu pelayar → *Install app*.
- **iPhone/iPad (Safari):** buka pautan → butang **Kongsi (Share)** → **Add to Home Screen**.
- **Komputer (Chrome/Edge):** ikon pasang (⊕) di bar alamat, atau butang dalam app.

Selepas dipasang, app boleh dibuka seperti aplikasi biasa dan berfungsi **luar talian**.

## Mengemas kini app
Bila anda ubah mana-mana fail:
1. Naikkan nombor versi di `sw.js` — tukar `math-heroes-v1` kepada `math-heroes-v2` (dan seterusnya).
2. Muat naik semula fail ke GitHub.
Service worker akan buang cache lama dan muat versi baharu secara automatik.

## Nota
- Progres murid, papan markah & tetapan bunyi disimpan dalam peranti (localStorage) — kekal walaupun luar talian.
- Papan markah adalah **per-peranti** (sesuai untuk tablet kelas yang dikongsi). Tukar nama wira sebelum main untuk merekod markah pemain berbeza.
- Untuk uji di komputer sendiri sebelum deploy: jalankan `python3 -m http.server` dalam folder ini, kemudian buka `http://localhost:8000`. (Service worker perlu HTTPS atau localhost — buka terus fail `index.html` tidak mengaktifkan mod luar talian.)

---
*Math Heroes • MISI SIFIR — JPN Kedah*

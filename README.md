# JustInfo News Portal - Blogger Template (Update 210226)

Template Blogger modern untuk portal berita dengan desain responsif, fitur lengkap, dan dioptimalkan untuk kenyamanan membaca di perangkat mobile.

## 📋 Fitur Utama

- ✅ **Mobile-First Reading Experience** (Layout tumpuk yang nyaman di HP)
- ✅ Breaking News Ticker (Berita Terkini Berjalan)
- ✅ Hero Slider (Slideshow Berita Utama)
- ✅ Iklan Global Responsif (Muncul di semua halaman)
- ✅ Featured Grid (Grid Berita Pilihan)
- ✅ Kategori dengan Layout Mixed (3 Grid + 2 List)
- ✅ Sidebar dengan Popular Posts & Archive
- ✅ Footer Dinamis (Logo, Social Media, Menu, Kontak)
- ✅ **Support Logo Footer** (Upload via Tata Letak)
- ✅ SEO Friendly & Fast Loading

---

## 🚀 Cara Install

1. Masuk ke **Blogger Dashboard**
2. Pilih blog Anda
3. Pergi ke **Tema** → **Sesuaikan** → **Edit HTML**
4. Hapus semua kode yang ada di editor
5. Salin seluruh isi file `template_210226.xml`
6. Tempel di editor HTML Blogger
7. Klik **Simpan** (Ikon Disket di pojok kanan atas)

---

## ⚙️ Konfigurasi Tata Letak (Layout)

### 1. Logo Header

**Lokasi:** Tata Letak → Header

- Klik widget **Header**
- Pilih **Upload gambar dari komputer**
- Atur penempatan (biasanya "Di belakang judul dan keterangan")
- Klik Simpan

### 2. Logo Footer (Fitur Baru)

**Lokasi:** Tata Letak → Footer (Kolom Pertama)

1. Cari section **footer-social** (di bawah widget "Tentang Kami")
2. Klik **Tambahkan Gadget**
3. Pilih **Gambar** (Image)
4. Judul: "Footer Logo" (opsional)
5. Upload gambar logo Anda
6. Klik **Simpan**
7. Seret/geser widget tersebut ke posisi di bawah widget Social Media jika perlu

---

### 3. Iklan Global Atas (Responsive)

**Lokasi:** Tata Letak → ad-before-slider (HTML99)

Iklan ini bersifat global dan muncul di posisi paling atas konten pada semua halaman (Homepage, Single Post, Static Page).

1. Klik **Edit** pada widget "Iklan Global Atas"
2. Tempel kode iklan AdSense atau banner Anda
3. Simpan

**Fitur:**
- Otomatis menyesuaikan ukuran layar (Responsive)
- Mengisi ruang kosong secara maksimal
- Mendukung script AdSense (ins/iframe) maupun banner gambar biasa.

---

### 4. Breaking News Ticker

Breaking News Ticker otomatis menampilkan postingan terbaru dari blog.

**Konfigurasi (Edit HTML):**

Cari kode berikut di template:
```javascript
loadTicker('breaking-ticker', '', 10);
```

Parameter:
- `'breaking-ticker'` - ID container (jangan diubah)
- `''` - Label filter (kosong = semua post, atau isi nama label)
- `10` - Jumlah post yang ditampilkan

**Mengatur Kecepatan Ticker:**

Untuk mempercepat atau memperlambat jalannya tulisan, cari kode CSS berikut di dalam template:
```css
.ticker{display:flex;animation:ticker 30s linear infinite;white-space:nowrap}
```
Ubah nilai `30s` (30 detik) menjadi lebih kecil untuk mempercepat (misal: `15s`) atau lebih besar untuk memperlambat (misal: `45s`).

**Contoh penggunaan:**
```javascript
// Menampilkan 10 post terbaru dari semua label
loadTicker('breaking-ticker', '', 10);

// Menampilkan 5 post dari label BREAKING saja
loadTicker('breaking-ticker', 'BREAKING', 5);
```

---

### 5. Hero Slider (Headline)

Hero Slider otomatis menampilkan postingan terbaru dengan gambar besar.

**Konfigurasi (Edit HTML):**

Cari kode berikut di template:
```javascript
loadSlider('main-slider', '', 5);
```

Parameter:
- `'main-slider'` - ID container (jangan diubah)
- `''` - Label filter (kosong = semua post, atau isi nama label)
- `5` - Jumlah slide yang ditampilkan

**Contoh penggunaan:**
```javascript
// Menampilkan 5 post terbaru dari semua label
loadSlider('main-slider', '', 5);

// Menampilkan 4 post dari label HEADLINE saja
loadSlider('main-slider', 'HEADLINE', 4);
```

---

### 6. Widget Kategori & Iklan di Homepage

**Lokasi:** Tata Letak → homepage-content

Section ini mendukung 2 jenis widget:

#### ➕ Menambah Widget KATEGORI:
1. Klik **Tambah Gadget** di section "homepage-content"
2. Pilih **HTML/JavaScript**
3. Isi:
   - **Judul**: Nama kategori yang tampil (contoh: "POLITIK")
   - **Konten**: Nama label persis (teks saja, tanpa HTML)
   
   Contoh: `POLITIK` atau `OLAHRAGA`
4. Simpan

#### ➕ Menambah Widget IKLAN:
1. Klik **Tambah Gadget** di section "homepage-content"
2. Pilih **HTML/JavaScript**
3. Isi:
   - **Judul**: "IKLAN" (opsional)
   - **Konten**: Kode HTML/Script iklan
   
   Contoh konten iklan:
   ```html
   <script async src="https://pagead2.googlesyndication.com/..."></script>
   <ins class="adsbygoogle" ...></ins>
   ```
4. Simpan

#### 📌 Cara Template Membedakan:
- Jika **konten mengandung tag HTML** (`<`) → ditampilkan sebagai **IKLAN**
- Jika **konten hanya teks biasa** → ditampilkan sebagai **KATEGORI**

---

### 7. Menu Navigasi

**Lokasi:** Tata Letak → Navigation (LinkList1)

Tambahkan link menu dengan format:

| Nama | URL |
|------|-----|
| Beranda | / |
| Daerah | `/search/label/DAERAH` |
| Olahraga | `/search/label/OLAHRAGA` |

---

### 8. Footer - Social Media

**Lokasi:** Tata Letak → footer-social (LinkList3)

Tambahkan link social media dengan format nama yang mengandung kata kunci:

| Nama | URL | Ikon |
|------|-----|------|
| Facebook | https://facebook.com/username | 🔵 Facebook |
| Twitter / X | https://twitter.com/username | ✖️ X (Twitter) |
| Instagram | https://instagram.com/username | 📷 Instagram |
| YouTube | https://youtube.com/channel/xxx | ▶️ YouTube |
| TikTok | https://tiktok.com/@username | 🎵 TikTok |
| WhatsApp | https://wa.me/62xxx | 💬 WhatsApp |
| Telegram | https://t.me/username | ✈️ Telegram |

---

## 🔤 Kustomisasi Font & Warna

Template ini mendukung pengaturan font dan warna yang mudah melalui CSS Variables.

### Mengubah Warna:
Cari bagian `:root` di dalam template (CSS):
```css
:root{
  --accent:#0d47a1;      /* Warna biru utama */
  --accent2:#e63946;     /* Warna merah aksen */
  --primary:#1a237e;     /* Warna biru gelap header */
  --bg:#f5f5f5;          /* Warna background */
}
```

### Mengubah Font:
Cari bagian `/* KONFIGURASI FONT */` atau edit variable di `:root`:
```css
:root{
  /* Font Default */
  --font-primary:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
```

---

## 📱 Tampilan Mobile

Template ini sudah dioptimalkan untuk kenyamanan membaca di ponsel:
- **Layout Tumpuk (Stacked)**: Berita ditampilkan 1 kolom penuh dengan gambar besar di atas dan judul di bawah, mirip aplikasi berita modern.
- **Font Terbaca**: Ukuran font disesuaikan (17-18px) agar nyaman di mata tanpa perlu zoom.
- **Navigasi Swipe**: Menu atas bisa digeser kanan-kiri.
- **Sidebar Tersembunyi**: Sidebar (kecuali widget penting) disembunyikan di mobile agar fokus ke konten.

---

## 🆘 Troubleshooting

**Q: Saya tidak bisa memulihkan tema (Error "Could not restore theme")?**
A: Gunakan file `template_210226.xml` yang sudah diperbaiki strukturnya. Jika masih gagal, hapus widget yang mungkin menyebabkan konflik (seperti logo footer) dari kode XML, lalu tambahkan secara manual lewat Tata Letak.

**Q: Logo footer tidak muncul?**
A: Pastikan Anda sudah menambahkan widget **Gambar** secara manual di Tata Letak bagian Footer (footer-social) setelah menginstall tema.

**Q: Komentar Facebook tidak muncul?**
A: Pastikan blog Anda sudah online dan tidak diblokir oleh adblocker browser.

---
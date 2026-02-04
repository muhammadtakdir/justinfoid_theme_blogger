# JustInfo News Portal - Blogger Template

Template Blogger modern untuk portal berita dengan desain responsif dan mudah dikonfigurasi.

## 📋 Fitur Utama

- ✅ Breaking News Ticker (Berita Terkini Berjalan)
- ✅ Hero Slider (Slideshow Berita Utama)
- ✅ Featured Grid (Grid Berita Pilihan)
- ✅ Kategori dengan Layout Mixed (3 Grid + 2 List)
- ✅ Sidebar dengan Popular Posts & Archive
- ✅ Footer yang bisa diedit dari Tata Letak
- ✅ Desain Responsif (Mobile Friendly)
- ✅ SEO Friendly

---

## 🚀 Cara Install

1. Masuk ke **Blogger Dashboard**
2. Pilih blog Anda
3. Pergi ke **Tema** → **Sesuaikan** → **Edit HTML**
4. Hapus semua kode yang ada
5. Salin seluruh isi file `template.xml`
6. Tempel di editor HTML Blogger
7. Klik **Simpan**

---

## ⚙️ Konfigurasi

### 1. Header & Logo

**Lokasi:** Tata Letak → Header

- Klik widget **Header** untuk mengubah judul dan deskripsi blog
- Untuk logo gambar, upload melalui pengaturan header

---

### 2. Breaking News Ticker

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

**Contoh penggunaan:**
```javascript
// Menampilkan 10 post terbaru dari semua label
loadTicker('breaking-ticker', '', 10);

// Menampilkan 5 post dari label BREAKING saja
loadTicker('breaking-ticker', 'BREAKING', 5);

// Menampilkan 8 post dari label HEADLINE
loadTicker('breaking-ticker', 'HEADLINE', 8);
```

---

### 3. Hero Slider (Headline)

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

// Menampilkan 6 post dari label UTAMA
loadSlider('main-slider', 'UTAMA', 6);
```

---

### 4. Iklan Atas Header (AdSense)

**Lokasi:** Tata Letak → ad-top (HTML99)

1. Klik **Edit** pada widget "Iklan Atas"
2. Tempel kode iklan AdSense atau banner Anda
3. Simpan

Contoh kode AdSense:
```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXX"
     data-ad-slot="XXXXXXXX"
     data-ad-format="auto"></ins>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
```

---

### 5. Menu Navigasi

**Lokasi:** Tata Letak → Navigation (LinkList1)

Tambahkan link menu dengan format:

| Nama | URL |
|------|-----|
| Beranda | / |
| Daerah | /search/label/DAERAH |
| Olahraga | /search/label/OLAHRAGA |
| Edukasi | /search/label/EDUKASI |
| Gaya Hidup | /search/label/GAYA%20HIDUP |

---

### 6. Widget Kategori & Iklan di Homepage

**Lokasi:** Tata Letak → homepage-content

Section ini mendukung 2 jenis widget:

#### ➕ Menambah Widget KATEGORI:
1. Klik **Tambah Gadget** di section "homepage-content"
2. Pilih **HTML/JavaScript**
3. Isi:
   - **Judul**: Nama kategori yang tampil (contoh: "DAERAH")
   - **Konten**: Nama label persis (teks saja, tanpa HTML)
   
   Contoh: `DAERAH` atau `OLAHRAGA`
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

#### ⚠️ Penting:
- Nama label di konten HARUS sama persis dengan label di blog (huruf besar/kecil)
- Anda bisa mengatur urutan widget dengan drag & drop di Tata Letak

---

### 7. Footer - Tentang Kami

**Lokasi:** Tata Letak → footer-about (Text1)

1. Klik **Edit** pada widget Text
2. Isi **Judul**: Tentang Kami
3. Isi **Konten**: Deskripsi website Anda

---

### 8. Footer - Social Media

**Lokasi:** Tata Letak → footer-social (LinkList3)

Tambahkan link social media dengan format nama yang mengandung kata kunci:

| Nama | URL | Ikon |
|------|-----|------|
| Facebook | https://facebook.com/username | 🔵 Facebook |
| Twitter | https://twitter.com/username | 🐦 Twitter |
| Instagram | https://instagram.com/username | 📷 Instagram |
| YouTube | https://youtube.com/channel/xxx | ▶️ YouTube |
| TikTok | https://tiktok.com/@username | 🎵 TikTok |
| WhatsApp | https://wa.me/62xxx | 💬 WhatsApp |
| Telegram | https://t.me/username | ✈️ Telegram |

**Penting:** Nama link HARUS mengandung kata kunci (Facebook, Twitter, dll) agar ikon muncul.

---

### 9. Footer - Kontak

**Lokasi:** Tata Letak → footer-contact (LinkList4)

Tambahkan informasi kontak dengan format:

| Nama | URL |
|------|-----|
| Email: info@domain.com | mailto:info@domain.com |
| Telepon: +62 123 456 789 | tel:+62123456789 |
| WhatsApp: +62 852 xxxx | https://wa.me/62852xxxx |
| Alamat: Jakarta, Indonesia | # |

**Kata kunci untuk ikon:**
- `Email` → Ikon amplop
- `Phone` atau `Telepon` → Ikon telepon
- `WhatsApp` → Ikon WhatsApp
- `Address` atau `Alamat` → Ikon lokasi

---

### 10. Footer - Menu

**Lokasi:** Tata Letak → footer-menu (LinkList2)

Tambahkan link halaman statis:

| Nama | URL |
|------|-----|
| Tentang Kami | /p/tentang-kami.html |
| Kebijakan Privasi | /p/kebijakan-privasi.html |
| Kontak | /p/kontak.html |
| Disclaimer | /p/disclaimer.html |

---

### 11. Footer - Kategori/Label

**Lokasi:** Tata Letak → footer-labels (Label3)

Widget ini otomatis menampilkan label/kategori dari blog Anda.
Tidak perlu konfigurasi manual.

---

### 12. Sidebar Homepage

**Lokasi:** Tata Letak → sidebar-home

Sidebar ini **hanya muncul di halaman utama, arsip, dan pencarian**.

**Widget default:**
- PopularPosts1 - Berita Populer
- HTML10 - Trending Posts
- Label1 - Kategori (List)
- BlogArchive1 - Arsip

Anda bisa menambah/hapus widget sesuai kebutuhan.

---

### 13. Sidebar Single Post

**Lokasi:** Tata Letak → sidebar-post

Sidebar ini **hanya muncul di halaman artikel (single post) dan static page**.

**Widget default:**
- PopularPosts2 - Artikel Populer
- HTML11 - Sedang Trending
- Label2 - Tags (Cloud)
- HTML12 - Slot Iklan Sidebar

Anda bisa menambah/hapus widget sesuai kebutuhan. Cocok untuk memasang iklan kontekstual yang hanya muncul di halaman artikel.

---

### 14. Related Posts (Berita Terkait)

Di halaman single post, secara otomatis menampilkan **5 artikel terkait** berdasarkan label pertama dari post tersebut.

Artikel ditampilkan dalam layout **grid 5 kolom** (responsive: 2 kolom di tablet, 1 kolom di mobile).

---

### 15. Komentar Facebook

Template ini menggunakan **Facebook Comments** sebagai sistem komentar.

**Keuntungan:**
- Pengguna bisa komentar menggunakan akun Facebook
- Mengurangi spam
- Integrasi sosial lebih baik

**Catatan:** Komentar akan muncul otomatis di halaman artikel.

---

## 🎨 Kustomisasi Warna

Untuk mengubah warna tema, edit bagian CSS Variables di template:

```css
:root{
  --accent:#0d47a1;      /* Warna biru utama */
  --accent2:#e63946;     /* Warna merah aksen */
  --primary:#1a237e;     /* Warna biru gelap */
  --bg:#f5f5f5;          /* Warna background */
  --card:#fff;           /* Warna card */
  --text:#333;           /* Warna teks */
  --muted:#777;          /* Warna teks secondary */
}
```

---

## 📝 Membuat Postingan

### Tips untuk tampilan optimal:

1. **Gunakan Label** - Setiap post harus memiliki minimal 1 label
2. **Gambar Utama** - Upload gambar di awal post untuk thumbnail
3. **Judul Menarik** - Maksimal 60-70 karakter
4. **Meta Description** - Isi deskripsi pencarian di pengaturan post

---

## ❓ FAQ

**Q: Kenapa kategori tidak muncul?**
A: Pastikan konten widget (bukan judul) sama persis dengan nama label di blog, termasuk huruf besar/kecil.

**Q: Kenapa muncul pesan "Silakan isi nama label di konten widget"?**
A: Widget kategori membutuhkan nama label di bagian konten. Edit widget dan isi konten dengan nama label yang tepat.

**Q: Kenapa ikon social media tidak muncul?**
A: Pastikan nama link mengandung kata kunci yang tepat (Facebook, Twitter, dll).

**Q: Bagaimana cara menambah kategori baru?**
A: 
1. Buka **Tata Letak**
2. Cari section **homepage-content**
3. Klik **Tambah Gadget** → pilih **HTML/JavaScript**
4. Isi Judul dengan nama kategori (contoh: "POLITIK")
5. Isi Konten dengan nama label persis (contoh: "POLITIK")
6. Simpan

**Q: Bagaimana cara memasang iklan AdSense?**
A: 
1. Buka **Tata Letak**
2. Klik **Edit** pada widget "Iklan Atas" (ad-top)
3. Tempel kode AdSense Anda
4. Simpan

---

## 📄 Lisensi

Template ini gratis digunakan untuk keperluan pribadi maupun komersial.
Kredit tidak wajib namun sangat dihargai.

---

## 🆘 Dukungan

Jika ada pertanyaan atau masalah, silakan hubungi pengembang.

---

**Dibuat dengan ❤️ untuk Blogger Indonesia**

# Praktikum 6 - Web Framework (Bootstrap)

**Nama:** Anggriani Hermawan  
**NIM:** 312410175  
**Kelas:** TI.24.A2  

---

### Langkah 1 — Membuat file HTML dasar
**Kode (index.html — tahap awal):**
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Praktikum 6 - Web Framework</title>
</head>
<body>
  <h1>Hello, Praktikum 6!</h1>
</body>
</html>
```
**Penjelasan:**
- Membuat kerangka dasar dokumen HTML5.  
- `<!DOCTYPE html>` menandakan dokumen HTML5.  
- `lang="id"` membantu mesin pencari dan pembaca layar mengetahui bahasa halaman.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 125440" src="https://github.com/user-attachments/assets/f159c232-0f3c-4c82-9093-15f7e19d9ce9" />

---

### Langkah 2 — Menambahkan Bootstrap (CDN)
**Kode (tambahkan di dalam `<head>` dan sebelum `</body>`):**
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
...
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

**Penjelasan:**
- Menghubungkan Bootstrap melalui CDN membuat kita bisa menggunakan class Bootstrap tanpa men-download file.
- CSS CDN untuk styling, JS bundle untuk interaksi (mis. navbar collapse).

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 125514" src="https://github.com/user-attachments/assets/bea8a255-c53c-44d4-9a1b-18795aee979e" />

---

### Langkah 3 — Menambahkan Navbar
**Kode (letakkan di dalam `<body>` paling atas):**
```html
<nav class="navbar navbar-expand-lg navbar-dark" style="background:#f07ea4;">
  <div class="container">
    <a class="navbar-brand fw-bold" href="#">SweetWeb</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="nav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link active" href="#">Beranda</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Artikel</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Kontak</a></li>
      </ul>
    </div>
  </div>
</nav>
```

**Penjelasan:**
- Navbar memungkinkan navigasi antar bagian.  
- Class `navbar-expand-lg` membuat navbar responsive (akan berubah menjadi tombol hamburger pada layar kecil).  
- `navbar-dark` cocok digunakan saat background gelap.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 125623" src="https://github.com/user-attachments/assets/bb0ed67f-12b3-4e58-a2f9-2e9cfa34782e" />

---

### Langkah 4 — Menambahkan Hero / Header besar
**Kode:**
```html
<section class="text-center" style="background:linear-gradient(90deg,#f9bec7,#fde2e4);padding:70px 0;border-bottom-left-radius:30px;border-bottom-right-radius:30px;">
  <div class="container">
    <h1 class="display-5 fw-bold">Halo, Selamat Datang </h1>
    <p class="lead">Belajar Bootstrap dengan desain manis dan lembut.</p>
    <a class="btn" style="background:#f68989;color:#fff;border-radius:10px;padding:8px 18px;">Mulai Sekarang</a>
  </div>
</section>
```

**Penjelasan:**
- Hero berfungsi sebagai area pertama yang dilihat pengunjung: menonjolkan pesan utama.  
- Menggunakan `display-5` dan `lead` dari Bootstrap untuk ukuran dan penekanan teks.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 125929" src="https://github.com/user-attachments/assets/ffc20b87-7117-4ebc-becb-f353bc9287d7" />

---

### Langkah 5 — Menambahkan Struktur Konten (Grid 2 Kolom)
**Kode:**
```html
<div class="container my-5">
  <div class="row g-4">
    <div class="col-md-8">
      <h3 class="fw-bold">Artikel Utama</h3>
      <p>Bootstrap mempermudah pembuatan layout responsif.</p>

      <div class="card p-4 mt-3" style="border-radius:12px;box-shadow:0 3px 10px rgba(0,0,0,0.08);">
        <h5 style="color:#f68989;">Card Contoh</h5>
        <p>Contoh penggunaan card Bootstrap dengan tema pink.</p>
        <a class="btn" style="background:#f9bec7;color:#fff;border-radius:8px;">Baca Selengkapnya</a>
      </div>
    </div>

    <div class="col-md-4">
      <h4 class="fw-bold">Menu Samping</h4>
      <ul class="list-group mb-3">
        <li class="list-group-item" style="background:#ffeef2;border:none;">Tutorial HTML</li>
        <li class="list-group-item" style="background:#ffeef2;border:none;">Tutorial CSS</li>
        <li class="list-group-item" style="background:#ffeef2;border:none;">Tutorial JS</li>
      </ul>

      <div class="p-3" style="background:#fff0f4;border-radius:10px;">
        <strong>Tips:</strong> gunakan warna lembut untuk tampilan nyaman.
      </div>
    </div>
  </div>
</div>
```

**Penjelasan:**
- Menggunakan grid Bootstrap (`row` dan `col-md-*`) untuk layout dua kolom.  
- `col-md-8` dan `col-md-4` membagi area menjadi 2/3 dan 1/3 pada layar medium ke atas; pada layar kecil akan otomatis menjadi satu kolom.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 130152" src="https://github.com/user-attachments/assets/1b47cdcc-7db1-45a8-9c42-8d4661da3853" />

---

### Langkah 6 — Menambahkan Footer
**Kode:**
```html
<footer style="background:#f07ea4;color:#fff;text-align:center;padding:18px 0;border-top-left-radius:18px;border-top-right-radius:18px;">
  <p class="mb-0">&copy; 2025 Praktikum 6 Web Framework | Desain oleh Anggriani</p>
</footer>
```

**Penjelasan:**
- Footer menutup halaman dan berfungsi menyertakan hak cipta atau informasi kontak.  
- Gaya sederhana agar sejalan dengan tema warna.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 130244" src="https://github.com/user-attachments/assets/eb60b047-d0ac-4d74-bc55-a5408aa68a42" />

---

### Langkah 7 — Perbaikan Estetika (Tambahan CSS di `<head>`)
**Kode (contoh CSS singkat, letakkan di `<head>` dalam `<style>`):**
```html
<style>
  body { background:#fff7fb; color:#42393a; font-family: Arial, sans-serif; }
  .navbar { background:#e96f97 !important; }
  .navbar .nav-link { color:#fff !important; }
  .btn { transition: .2s; }
</style>
```

**Penjelasan:**
- Memperhalus tampilan dengan memilih font, warna latar, dan transisi pada tombol.  
- Perubahan ini membuat tampilan lebih konsisten dan profesional.

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 130536" src="https://github.com/user-attachments/assets/101af47b-70b1-4670-8c0f-8be1105eb6cc" />

---

### HASIL OUTPUT AKHIR
**Penjelasan:**
- Menghapus teks "Hello, Praktikum 6!"
    
<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 132233" src="https://github.com/user-attachments/assets/7d3928db-f923-47ed-8c6e-813268f4ded8" />

---

### Langkah 8 — Validasi HTML (W3C)
**Langkah validasi:**
1. Buka: https://validator.w3.org  
2. Pilih tab **Validate by File Upload** atau **Direct Input**.  
3. Upload `index.html` atau paste isi file lalu klik **Check**.

**Penjelasan:**
- Validasi memastikan struktur HTML sesuai standar sehingga mengurangi masalah kompatibilitas.  

<img width="1920" height="1080" alt="Cuplikan layar 2025-10-27 132730" src="https://github.com/user-attachments/assets/00b0739f-9fc8-4687-af2a-cee556a6a3e0" />

---

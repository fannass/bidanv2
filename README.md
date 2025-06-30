# 🏥 Website Puskesmas COMORO (Timor Leste)

Website statis untuk Puskesmas COMORO di wilayah Timor Leste yang menyediakan informasi layanan kesehatan dan fitur pendaftaran pasien secara digital. **Website ini telah dioptimalkan untuk responsif di semua perangkat.**

## 🌟 Fitur Utama

### 📄 Halaman Website
1. **Beranda (index.html)** - Sambutan dan layanan utama
2. **Tentang (about.html)** - Informasi puskesmas dan fasilitas
3. **Layanan (services.html)** - Daftar lengkap layanan kesehatan
4. **Registrasi Pasien (register.html)** - Form pendaftaran pasien dummy
5. **Kritik & Saran (feedback.html)** - Form feedback dari masyarakat
6. **Login Admin (login.html)** - Halaman login untuk administrator
7. **Dashboard (dashboard.html)** - Panel admin dengan data dummy

### 🌐 Multi-Bahasa
Mendukung 3 bahasa:
- 🇮🇩 **Bahasa Indonesia** (default)
- 🇬🇧 **English**
- 🇹🇱 **Tetun** (Bahasa Timor Leste)

### 🏥 Layanan yang Tersedia
- **Rawat Jalan** - Pemeriksaan dan pengobatan tanpa menginap
- **Unit Gawat Darurat** - Pelayanan darurat 24 jam
- **Kesehatan Ibu & Anak** - KIA, persalinan, dan tumbuh kembang
- **Imunisasi & KB** - Program imunisasi dan keluarga berencana

## 📱 Responsive Design Features

### 🎯 Mobile-First Approach
Website ini dirancang dengan pendekatan mobile-first untuk memastikan pengalaman terbaik di semua perangkat:

#### 📱 Mobile Navigation
- **Hamburger Menu**: Menu hamburger dengan overlay slide-in dari kanan
- **Touch-Friendly**: Tombol dan elemen yang mudah disentuh (minimum 44px)
- **Smooth Animations**: Transisi halus untuk menu dan overlay
- **Backdrop Blur**: Efek blur pada background saat menu terbuka
- **Body Scroll Prevention**: Mencegah scroll body saat menu terbuka

#### 📐 Responsive Breakpoints
```css
/* Large Tablets and Small Laptops */
@media (max-width: 1024px) { ... }

/* Tablets */
@media (max-width: 768px) { ... }

/* Mobile Phones */
@media (max-width: 480px) { ... }

/* Extra Small Mobile */
@media (max-width: 360px) { ... }

/* Landscape Mobile */
@media (max-height: 500px) and (orientation: landscape) { ... }
```

#### 🎨 Responsive Components

**Header & Navigation**
- Logo yang menyesuaikan ukuran
- Navigation yang berubah menjadi hamburger menu di mobile
- Language switcher yang responsif
- User info section yang fleksibel

**Grid Layouts**
- Services grid: `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))`
- Stats grid: Responsif dengan 1-4 kolom berdasarkan screen size
- Form layouts: Single column di mobile, multi-column di desktop

**Forms**
- Input fields dengan `font-size: 16px` untuk mencegah zoom di iOS
- Touch-friendly buttons dan form elements
- Responsive form validation messages
- Optimized spacing untuk mobile

**Tables**
- Horizontal scroll untuk tabel di mobile
- Responsive column widths
- Touch-friendly table interactions

**Cards & Sections**
- Service cards yang fleksibel
- Consistent spacing dan padding
- Optimized untuk touch interaction
- Smooth hover effects

### 🚀 Performance Optimizations

**Mobile Performance**
- Optimized images dan assets
- Efficient CSS media queries
- Fast loading pada mobile networks
- Minimal JavaScript untuk mobile

**Accessibility**
- Semantic HTML structure
- Proper heading hierarchy
- Alt text untuk images
- Keyboard navigation support
- Screen reader friendly
- High contrast ratios

## 🗂️ Struktur Folder

```
bidan-comoro/
├── index.html           # Halaman beranda
├── about.html           # Halaman tentang puskesmas
├── services.html        # Daftar layanan
├── signup.html          # Halaman daftar akun baru
├── login.html           # Halaman login
├── register.html        # Form registrasi pasien (protected)
├── feedback.html        # Form kritik dan saran (protected)
├── user-dashboard.html  # Dashboard untuk user
├── dashboard.html       # Dashboard administrator (admin only)
├── style.css            # CSS utama
├── lang.js              # JavaScript multi-bahasa & auth
├── README.md            # Dokumentasi ini
└── assets/
    └── flags/
        ├── README.md    # Petunjuk gambar bendera
        ├── indonesia.png    (opsional)
        ├── english.png      (opsional)
        └── tetun.png        (opsional)
```

## 🎨 Desain & UI/UX

### Warna Tema
- **Hijau Pastel**: #A8D5BA (warna utama)
- **Hijau Tua**: #7CB085 (aksen)
- **Putih**: #FFFFFF (background)
- **Abu Terang**: #F4F4F4 (background sekunder)

### Font
- **Primary**: Poppins (dari Google Fonts)
- **Fallback**: Arial, sans-serif

### Responsive Design
- Mobile-first approach
- Breakpoints: 768px (tablet), 480px (mobile)
- Flexbox dan CSS Grid untuk layout

## 🔧 Teknologi

- **HTML5** - Struktur dan konten
- **CSS3** - Styling dan responsivitas
- **JavaScript ES6** - Interaktivitas dan multi-bahasa
- **No Framework** - Vanilla JavaScript/CSS
- **No Backend** - Website statis

## 🚀 Cara Menjalankan

1. **Download/Clone** folder website
2. **Buka browser** (Chrome, Firefox, Edge, dll.)
3. **Drag & drop** file `index.html` ke browser
   
   ATAU
   
   Klik kanan `index.html` → "Open with" → Pilih browser

4. **Website siap digunakan!**

## ⚡ Fitur JavaScript

### Multi-Language System
```javascript
// Ganti bahasa
changeLanguage('id');  // Indonesia
changeLanguage('en');  // English
changeLanguage('tet'); // Tetun
```

### Form Validation (Dummy)
- Validasi input required
- Simulasi submit berhasil
- Local storage untuk bahasa

### Dashboard Features
- Tabel data pasien dengan pagination
- Filter status pasien
- Mock data dan statistik
- Auto-refresh simulation

## 🔐 Sistem Autentikasi

Website ini menggunakan sistem login berbasis role untuk membedakan akses user dan admin:

### 👥 Role & Akses:
- **Admin**: Akses ke Dashboard Admin untuk mengelola puskesmas
- **User**: Akses ke Dashboard User, form registrasi, dan feedback

### 🔑 Demo Credentials:
- **Admin**: username: `admin` | password: `admin123`
- **User**: username: `user1` | password: `user123`

### 📋 Alur Autentikasi:
1. **Pengguna baru** → Daftar akun di halaman Signup
2. **Login** → Masuk dengan username/password
3. **Redirect otomatis** berdasarkan role:
   - Admin → Dashboard Admin
   - User → Dashboard User
4. **Proteksi halaman**:
   - Registrasi pasien → Hanya user yang login
   - Feedback → Hanya user yang login  
   - Dashboard Admin → Hanya admin
   - Dashboard User → Hanya user yang login

### 🛡️ Fitur Keamanan:
- Session storage menggunakan localStorage
- Auto-redirect jika sudah login
- Proteksi halaman berdasarkan role
- Logout dengan clear session
- Navigation dinamis berdasarkan status login

## 📱 Responsive Features

### Desktop (1200px+)
- Layout grid 4 kolom
- Navigation horizontal
- Sidebar dan main content

### Tablet (768px - 1199px)
- Layout grid 2-3 kolom
- Navigation tetap horizontal
- Komponen lebih besar

### Mobile (< 768px)
- Layout single column
- Navigation vertical/collapsed
- Touch-friendly buttons

## 🎯 Fitur Khusus

### Forms
- **Registrasi Pasien**: Data pribadi, medis, kontak darurat
- **Feedback**: Rating, kategori, saran perbaikan
- **Login**: Autentikasi admin dengan demo credentials

### Dashboard Admin
- **Statistik Real-time**: Pasien baru, kunjungan, darurat
- **Tabel Pasien**: Pagination, filter, export
- **Charts**: Placeholder untuk integrasi Chart.js
- **Feedback Monitor**: Feedback terbaru dari masyarakat

### Language Switch
- **Persistent**: Tersimpan di localStorage
- **Real-time**: Update tanpa reload halaman
- **Complete**: Semua text element ter-translate

## 🌐 Browser Support

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ⚠️ Internet Explorer (tidak disarankan)

## 📝 Catatan Penting

### Dummy Features
- Semua form adalah **dummy** (tidak menyimpan data)
- Login **simulasi** saja (tidak ada backend)
- Dashboard menggunakan **mock data**
- Tidak ada koneksi database

### Real Implementation
Untuk implementasi nyata diperlukan:
- Backend server (PHP, Node.js, Python, dll.)
- Database (MySQL, PostgreSQL, dll.)
- Autentikasi sesungguhnya
- Form validation server-side
- API untuk data management

## 🚑 Kontak Darurat

**Puskesmas COMORO**
- 📍 COMORO, Timor-Leste
- 📞 +670 123 456 789 (24 Jam)
- 📧 info@puskes-comoro.tl

## 📄 Lisensi

© 2025 Puskesmas COMORO, Timor Leste. 
Website ini dibuat untuk keperluan edukasi dan demo.

---


**Terima kasih telah menggunakan website Puskesmas COMORO!** 🏥❤️

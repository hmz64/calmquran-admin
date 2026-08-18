# ☪️ CalmQuran — Admin Control Panel

Panel Admin modern untuk mengelola profil Qari (nama, photo, status popular) dan mengupload audio Surah MP3 secara langsung ke **Backblaze B2 Storage** (`calmquran-media`).

---

## 🚀 Fitur Admin Panel
1. **Manajemen Profil Qari**:
   - Tambah Qari baru (Nama, Slug, Foto, Status Popular).
   - Upload foto Qari otomatis ke Backblaze B2.
2. **Upload Audio Surah MP3**:
   - Pilih Qari & Surah (1 s/d 114).
   - Drag & Drop upload file audio MP3 langsung ke Backblaze B2 bucket (`surahs/{qari_slug}/{surah_number}.mp3`).
   - Live Audio Player Preview untuk langsung menguji hasil upload.
3. **Pilihan Server Dynamic**:
   - Beralih instan antara Server Production Railway (`https://calmquran.api.rinteractive.my.id`) atau Server Lokal (`http://localhost:8080`).

---

## 🌐 Panduan Deploy ke Vercel (1-Click Deployment)

### Opsi A: Deploy via GitHub (Otomatis & Gratis)
1. Buat repository baru di GitHub bernama `calmquran-admin`.
2. Push folder `calmquran-admin` ini ke GitHub repository tersebut:
   ```bash
   cd calmquran-admin
   git init
   git add .
   git commit -m "feat: initial calmquran admin panel"
   git remote add origin https://github.com/hmz64/calmquran-admin.git
   git push -u origin main
   ```
3. Buka [Vercel Dashboard](https://vercel.com/dashboard) -> **Add New Project**.
4. Import repository `calmquran-admin`.
5. Klik **Deploy**! (Vercel akan selesai mem-publish dalam 5 detik).

---

### 🔗 Menghubungkan Subdomain Custom (misal: `admin.rinteractive.my.id` atau `calmquran-admin.rinteractive.my.id`):
1. Di Vercel Dashboard, buka **Project Settings** -> **Domains**.
2. Masukkan subdomain pilihan Anda (misal: `admin.rinteractive.my.id`).
3. Tambahkan DNS CNAME Record di provider Domain / Cloudflare Anda:
   * **Type**: `CNAME`
   * **Name**: `admin`
   * **Target**: `cname.vercel-dns.com`
4. Selesai! Panel Admin Anda langsung dapat diakses dari subdomain resmi Anda.

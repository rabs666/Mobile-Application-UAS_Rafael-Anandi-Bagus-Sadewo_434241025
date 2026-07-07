# 🎬 Naskah Video Demo (Santai) — E-Ticketing Helpdesk UTS

**Gaya:** ngobrol santai · **Fokus:** langkah rekam per klik · **Durasi:** ~5 menit

> Cara pakai: baris **▶️ KLIK** = yang kamu lakuin di HP (rekam ini). Baris **🎙️** = tinggal ngomong santai, ga usah plek-plekan.

---

## 🧾 Sebelum Rekam

**Akun (password semua `123456`):** `ahmad` (User) · `admin` (Admin) · `arif` (Helpdesk)

- [ ] HP ada internet (app pakai Supabase)
- [ ] APK versi terbaru (v5) udah keinstall
- [ ] Ada 1 foto di galeri buat demo lampiran
- [ ] Nyalain **"Show taps"** di Developer Options (biar keliatan jarinya)
- [ ] Habis klik tombol simpan/terima/selesai, **tunggu 1-2 detik** (nunggu internet)

---

## 1️⃣ INTRO (±20 detik)

**▶️ KLIK:** Buka app, biarin splash screen jalan, berhenti di halaman Login.

**🎙️** "Halo, aku Rafael, NIM 434241025. Di video ini aku bakal nunjukin aplikasi E-Ticketing Helpdesk buat UAS Mobile. App ini dibikin pakai Kotlin + Jetpack Compose, dan datanya udah nyambung ke Supabase online. Ada tiga user: pelapor, admin, sama helpdesk. Yuk langsung aja."

---

## 2️⃣ DAFTAR & LOGIN (±40 detik)

**▶️ KLIK:**
1. Di Login, tap **"Daftar"** / Register
2. Isi: Nama bebas, username bebas, email bebas, password (min 6)
3. Tap **Register** → balik ke Login

**🎙️** "Pertama, user baru bisa daftar dulu. Nih aku isi datanya... simpan. Datanya langsung masuk ke database Supabase ya, bukan cuma di HP."

**▶️ KLIK:**
4. Tap **"Lupa Password"** → ketik email → submit → balik
5. Login pakai **`ahmad`** / **`123456`**

**🎙️** "Ada juga fitur lupa password lewat email. Oke sekarang aku login sebagai Ahmad, dia user biasa alias pelapor."

---

## 3️⃣ USER: BUAT TIKET (±60 detik)

**▶️ KLIK:**
1. Diem sebentar di **Dashboard** — tunjuk kartu statistik (Open/Assigned/In Progress/Closed)

**🎙️** "Ini dashboard-nya Ahmad. Ada statistik tiket per status, sama badge notifikasi di pojok."

**▶️ KLIK:**
2. Masuk **Daftar Tiket** — tunjuk kalau isinya cuma tiket dia sendiri

**🎙️** "Di daftar tiket, user cuma bisa lihat tiket punya dia sendiri ya, ga bisa lihat punya orang lain."

**▶️ KLIK:**
3. Tap tombol **Buat Tiket**
4. Judul: **"Proyektor Ruang 101 Rusak"**
5. Deskripsi: **"Proyektor tidak menyala saat perkuliahan"**
6. Tap area **lampiran** → pilih **Galeri** (atau Kamera) → pilih 1 foto
7. Tap **Simpan & Kirim Tiket** → *(tunggu 2 detik)*

**🎙️** "Ahmad bikin tiket keluhan baru. Isi judul, deskripsi, terus bisa lampirin foto — bisa dari galeri atau motret langsung. Kirim. Nah tiketnya langsung nongol di daftar, statusnya OPEN."

**▶️ KLIK:**
8. Tap tiket yang baru dibuat → tunjuk **timeline** di bawah

**🎙️** "Kalau dibuka detailnya, ada timeline yang nyatet 'Tiket dibuat'. Ini bakal kepake buat ngelacak perjalanan tiket nanti."

---

## 4️⃣ ADMIN: TERIMA, ASSIGN, KELOLA USER (±80 detik)

**▶️ KLIK:**
1. Buka **Profil** → tap **Logout**
2. Login **`admin`** / **`123456`**

**🎙️** "Sekarang aku logout, terus login jadi Admin. Admin bisa lihat SEMUA tiket dari semua orang."

**▶️ KLIK:**
3. Masuk **Daftar Tiket** → buka tiket **"Proyektor Ruang 101 Rusak"** (masih OPEN)
4. Tap tombol **Terima Tiket** → *(tunggu 2 detik, status jadi ASSIGNED)*

**🎙️** "Aku buka tiket barunya Ahmad. Langkah pertama, admin klik Terima. Otomatis statusnya berubah jadi ASSIGNED."

**▶️ KLIK:**
5. Tap tombol **Assign / Tugaskan** → pilih **Arif Helpdesk** → *(tunggu 2 detik, status jadi IN PROGRESS)*

**🎙️** "Terus admin nugasin tiket ini ke petugas helpdesk, si Arif. Begitu di-assign, statusnya otomatis jadi IN PROGRESS. Gampang kan, ga usah ubah status manual."

**▶️ KLIK:**
6. Balik → **Profil** → tap kartu **Kelola Pengguna**
7. Tunjuk daftar user
8. Tap **Tambah** → isi form → pilih role (misal Helpdesk) → **Simpan**
9. Tap chip **role** salah satu user → ganti rolenya
10. Tap ikon **hapus** salah satu user → **konfirmasi**

**🎙️** "Nah ini fitur khusus admin: Kelola Pengguna. Admin bisa nambah user baru sambil milih perannya, ganti role user lain — misal naikin jadi helpdesk — sampai hapus user. Semua langsung kesimpen ke Supabase."

---

## 5️⃣ HELPDESK: KERJAIN & SELESAIIN (±60 detik)

**▶️ KLIK:**
1. **Logout** → login **`arif`** / **`123456`**
2. Buka halaman **Notifikasi** → tunjuk notif penugasan → tap buat tandai dibaca

**🎙️** "Ganti akun, sekarang jadi Arif si helpdesk. Dia dapet notifikasi ada tiket yang ditugasin ke dia."

**▶️ KLIK:**
3. Buka tiket **"Proyektor Ruang 101 Rusak"** (status IN PROGRESS)
4. Di kolom komentar, ketik: **"Sudah saya cek, kabelnya diganti. Coba dites lagi ya."** → kirim

**🎙️** "Arif buka tiket yang lagi dia kerjain. Dia bisa ngobrol sama pelapor lewat komentar. Komentar ini kesimpen di Supabase, jadi Ahmad bisa lihat juga."

**▶️ KLIK:**
5. Tap tombol **Selesai** → *(tunggu 2 detik, status jadi CLOSED)*

**🎙️** "Kalau udah beres, Arif klik Selesai. Statusnya otomatis jadi CLOSED. Tiket tuntas."

---

## 6️⃣ BALIK KE USER + DARK MODE (±40 detik)

**▶️ KLIK:**
1. **Logout** → login lagi **`ahmad`**
2. Buka **Notifikasi** → tunjuk notif "Tiket Selesai"
3. Buka **detail tiket** → tunjuk status **CLOSED** + timeline lengkap

**🎙️** "Balik lagi jadi Ahmad, buat buktiin datanya real-time. Dia dapet notif tiketnya udah selesai. Di detailnya, timeline-nya lengkap — dari dibuat, diterima, ditugasin, sampai selesai. Kelacak semua."

**▶️ KLIK:**
4. Buka **Profil** → nyalain toggle **Dark Mode**

**🎙️** "Terakhir, app-nya juga ada dark mode. Tinggal geser, langsung berubah semua."

---

## 7️⃣ PENUTUP (±15 detik)

**▶️ KLIK:** Balik ke Dashboard (mode gelap), diem sebentar.

**🎙️** "Yak segitu aja demo E-Ticketing Helpdesk-nya. Udah lengkap: login, buat tiket, empat status tiket, kelola user, komentar, notifikasi, sama dark mode — semua nyambung ke Supabase. Makasih udah nonton!"

---

## ✅ Ceklis biar ga ada yang kelewat
Auth: `daftar` `login` `lupa password` `logout` · User: `dashboard` `daftar tiket` `buat tiket` `lampiran` `timeline` · Admin: `terima` `assign` `kelola user (tambah/role/hapus)` · Helpdesk: `notifikasi` `komentar` `selesai` · Umum: `dark mode`

## 💡 Tips
- Rekam **per bagian** (1–7) terpisah, gampang ngulang kalau salah.
- Kalau internet lemot, jeda dikit habis klik biar datanya kekejar.
- Mau lebih meyakinkan? Split-screen sama dashboard Supabase yang datanya ikut berubah.

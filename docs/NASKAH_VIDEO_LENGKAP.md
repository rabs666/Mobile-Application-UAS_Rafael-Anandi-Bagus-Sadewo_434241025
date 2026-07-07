# 🎬 Naskah Video Demo LENGKAP — E-Ticketing Helpdesk UTS

**Durasi estimasi:** 5–7 menit
**Target:** Dosen Penilai UAS Mobile (Teori & Praktikum)
**Format:** Screen recording HP + voice over (narasi)

---

## 🧾 Persiapan Sebelum Rekam

**Akun demo (password semua: `123456`):**

| Username | Role | Nama | Dipakai untuk |
|----------|------|------|---------------|
| `ahmad` | USER | Ahmad Dani | Pelapor / buat tiket |
| `admin` | ADMIN | Admin UTS | Terima & assign tiket, kelola pengguna |
| `arif` | HELPDESK | Arif Helpdesk | Kerjakan & selesaikan tiket |

**Checklist sebelum mulai:**
- [ ] HP terkoneksi internet (app pakai Supabase real-time)
- [ ] Sudah install APK versi terbaru (v5 — auto-refresh)
- [ ] Siapkan 1 foto di galeri (untuk demo lampiran)
- [ ] (Opsional) buka dashboard Supabase di laptop untuk bukti data masuk

**Alur status yang akan didemokan:**
`OPEN` → (Admin **Terima**) → `ASSIGNED` → (Admin **Assign** helpdesk) → `IN_PROGRESS` → (Helpdesk **Selesai**) → `CLOSED`

---

## [00:00 – 00:35] 🎬 Opening & Perkenalan

**🎥 Visual:** Splash screen → halaman Login.

**🎙️ Narasi:**
> "Assalamualaikum / halo. Perkenalkan, saya Rafael Anandi Bagus Sadewo, NIM 434241025. Pada video ini saya akan mendemonstrasikan aplikasi **E-Ticketing Helpdesk** untuk UAS Mobile.
>
> Aplikasi ini dibangun dengan **Native Android — Kotlin dan Jetpack Compose**, arsitektur **MVVM**, dan sudah terintegrasi penuh dengan **backend Supabase (PostgreSQL)** secara real-time. Terdapat tiga peran pengguna: **User** sebagai pelapor, **Admin** sebagai pengelola, dan **Helpdesk** sebagai petugas."

**🎥 Visual (opsional):** Tampilkan sekilas tabel `tickets` & `users` di dashboard Supabase.
> "Ini database Supabase yang menyimpan data users, tickets, comments, activities, dan notifications."

---

## [00:35 – 01:15] 🔐 Fitur Autentikasi

**🎥 Visual:** Di halaman Login, klik "Daftar / Register".

**🎙️ Narasi:**
> "Pertama, fitur autentikasi. Pengguna baru dapat **mendaftar** melalui halaman registrasi."

**🎥 Visual:** Isi form Register (nama, username, email, password), submit → kembali ke Login.
> "Setiap registrasi divalidasi — cek duplikasi username dan email — lalu **disimpan langsung ke tabel `users` di Supabase**. Akun baru otomatis berperan sebagai User."

**🎥 Visual:** Klik "Lupa Password" → masukkan email → submit.
> "Tersedia juga fitur **reset password** melalui email terdaftar."

**🎥 Visual:** Kembali ke Login, login sebagai `ahmad` / `123456`.
> "Sekarang saya login sebagai User bernama Ahmad."

---

## [01:15 – 02:20] 👤 Skenario USER — Membuat & Memantau Tiket

**🎥 Visual:** Dashboard User tampil.

**🎙️ Narasi:**
> "Setelah login, User masuk ke **Dashboard** yang menampilkan **statistik tiket** berdasarkan status: Open, Assigned, In Progress, dan Closed. Terlihat juga badge notifikasi yang belum dibaca."

**🎥 Visual:** Buka daftar tiket → tunjukkan hanya tiket milik sendiri.
> "Di **Daftar Tiket**, User hanya melihat tiket miliknya sendiri. Daftar bisa difilter berdasarkan status."

**🎥 Visual:** Klik tombol Buat Tiket. Isi judul "Proyektor Ruang 101 Rusak", deskripsi "Proyektor tidak menyala saat perkuliahan".
> "User membuat tiket pengaduan baru. Isi judul dan deskripsi keluhan."

**🎥 Visual:** Klik area lampiran → pilih **Kamera** atau **Galeri** → pilih foto.
> "User juga bisa melampirkan bukti, baik memotret langsung dari **kamera** maupun memilih dari **galeri**."

**🎥 Visual:** Klik "Simpan & Kirim Tiket" → kembali ke daftar, tiket baru muncul berstatus OPEN.
> "Setelah dikirim, tiket tersimpan ke Supabase dengan status awal **OPEN**, dan langsung muncul di daftar."

**🎥 Visual:** Buka detail tiket yang baru dibuat → tunjukkan timeline.
> "Di **Detail Tiket** terdapat **timeline audit trail** yang mencatat setiap aktivitas — dimulai dari 'Tiket dibuat'."

---

## [02:20 – 03:30] 🛡️ Skenario ADMIN — Menerima, Menugaskan & Kelola Pengguna

**🎥 Visual:** Logout Ahmad → login `admin` / `123456`.

**🎙️ Narasi:**
> "Sekarang saya logout, lalu login sebagai **Admin**. Admin dapat melihat **seluruh tiket** dari semua pelapor."

**🎥 Visual:** Buka tiket "Proyektor Ruang 101 Rusak" (status OPEN).
> "Admin membuka tiket baru dari Ahmad. Sesuai alur bisnis, ada **empat langkah status**."

**🎥 Visual:** Klik tombol **Terima Tiket**. Status berubah OPEN → ASSIGNED.
> "**Langkah kedua:** Admin menekan **Terima**. Status otomatis berubah menjadi **ASSIGNED**, dan tercatat di timeline."

**🎥 Visual:** Klik **Assign / Tugaskan**, pilih petugas **Arif Helpdesk**.
> "**Langkah ketiga:** Admin menugaskan tiket ke petugas Helpdesk, yaitu Arif. Begitu di-assign, status otomatis menjadi **IN PROGRESS**."

**🎥 Visual:** Buka menu **Profil** → kartu **Kelola Pengguna**.
> "Selanjutnya, fitur khusus Admin: **Kelola Pengguna**."

**🎥 Visual:** Tampilkan daftar pengguna. Klik tombol **Tambah** → isi form + pilih role Helpdesk → Simpan.
> "Admin dapat **menambah pengguna baru** dengan memilih perannya secara langsung."

**🎥 Visual:** Klik chip role salah satu user → ubah rolenya.
> "Admin juga bisa **mengubah role** pengguna — misalnya menaikkan User biasa menjadi Helpdesk."

**🎥 Visual:** Klik ikon hapus pada satu user → konfirmasi.
> "Serta **menghapus pengguna**. Semua perubahan ini **langsung tersinkron ke tabel `users` Supabase**."

---

## [03:30 – 04:30] 🧰 Skenario HELPDESK — Menyelesaikan Tiket

**🎥 Visual:** Logout Admin → login `arif` / `123456`.

**🎙️ Narasi:**
> "Berikutnya saya login sebagai petugas **Helpdesk**, Arif. Ia menerima **notifikasi** bahwa ada tiket yang ditugaskan kepadanya."

**🎥 Visual:** Buka halaman Notifikasi → tunjukkan notif penugasan. Tandai dibaca.
> "Di halaman notifikasi, Arif melihat pemberitahuan penugasan dan bisa menandainya sebagai sudah dibaca."

**🎥 Visual:** Buka tiket "Proyektor Ruang 101 Rusak" (status IN_PROGRESS).
> "Arif membuka tiket yang sedang ia tangani — statusnya **In Progress**."

**🎥 Visual:** Tulis komentar "Sudah saya cek, kabel proyektor diganti. Silakan dites kembali." → kirim.
> "Arif berdiskusi dengan pelapor melalui **kolom komentar**. Komentar ini tersimpan di Supabase dan bisa dilihat pelapor secara real-time."

**🎥 Visual:** Klik tombol **Selesai**. Status berubah IN_PROGRESS → CLOSED.
> "**Langkah keempat:** setelah masalah teratasi, Arif menekan **Selesai**. Status tiket otomatis berubah menjadi **CLOSED**, menandakan tiket telah tuntas."

---

## [04:30 – 05:15] 🔁 Verifikasi dari Sisi User & Dark Mode

**🎥 Visual:** Logout Arif → login kembali `ahmad`.

**🎙️ Narasi:**
> "Untuk membuktikan sinkronisasi real-time, saya login kembali sebagai Ahmad, sang pelapor."

**🎥 Visual:** Buka notifikasi → ada notif "Tiket Selesai". Buka detail tiket → status CLOSED + timeline lengkap.
> "Ahmad menerima **notifikasi bahwa tiketnya telah selesai**. Di detail tiket, seluruh perjalanan tercatat lengkap di timeline: dibuat, diterima, ditugaskan, dikerjakan, hingga selesai — sebagai **audit trail** penuh."

**🎥 Visual:** Buka Profil → aktifkan toggle **Dark Mode**.
> "Terakhir, aplikasi mendukung **Mode Gelap** yang diterapkan secara global menggunakan Material 3."

---

## [05:15 – 05:45] 🎬 Penutup

**🎥 Visual:** Dashboard dalam Dark Mode → logo aplikasi.

**🎙️ Narasi:**
> "Demikian demonstrasi aplikasi E-Ticketing Helpdesk. Aplikasi ini telah memiliki alur helpdesk yang lengkap: autentikasi, siklus tiket empat status, manajemen pengguna, komentar, notifikasi, statistik, dan mode gelap — seluruhnya terintegrasi dengan **backend Supabase** secara real-time.
>
> Terima kasih. Wassalamualaikum / sekian."

---

## 📋 Checklist Fitur yang Tercakup (untuk memastikan tidak ada yang terlewat)

**Autentikasi**
- [x] Register (persist ke Supabase)
- [x] Login (3 role)
- [x] Reset password
- [x] Logout

**User (Pelapor)**
- [x] Dashboard statistik
- [x] Daftar tiket (difilter milik sendiri) + filter status
- [x] Buat tiket + lampiran (kamera/galeri)
- [x] Detail tiket + timeline audit trail
- [x] Komentar
- [x] Notifikasi

**Admin**
- [x] Lihat semua tiket
- [x] Terima tiket (OPEN → ASSIGNED)
- [x] Assign helpdesk (ASSIGNED → IN_PROGRESS)
- [x] Kelola Pengguna: tambah, ubah role, hapus

**Helpdesk**
- [x] Notifikasi penugasan
- [x] Lihat tiket yang ditangani
- [x] Komentar / respon
- [x] Selesaikan tiket (IN_PROGRESS → CLOSED)

**Umum**
- [x] Dark mode
- [x] Sinkronisasi real-time Supabase

---

### 💡 Tips Rekaman
1. **Rekam per-segmen** (login, user, admin, helpdesk terpisah) lalu gabung — lebih mudah kalau ada salah.
2. Aktifkan **"Show taps"** di Developer Options HP agar sentuhan terlihat di video.
3. Tunggu **1–3 detik** setelah aksi tulis (buat/terima/selesai) karena data lewat internet.
4. Bila mau bukti kuat: split screen dengan **dashboard Supabase** yang datanya ikut berubah.
5. Bicara **pelan & jelas**; boleh baca narasi apa adanya dari naskah ini.

# Day 1 – Proyek Workshop 26

**Nama Lengkap:** Khoirul Abdul Azis
**Kelompok:** GTA
**Kegiatan:** Day 1 Proyek Workshop-26 – *From AI to GitHub: Building with AI, Managing Change with GitHub*
**Pemateri:** Nugi Farhan (Senior Product Designer)
**Tanggal:** Sabtu, 7 November 2026

---

## Deskripsi Repository
Repository ini berisi dokumentasi kegiatan Day 1 Proyek Workshop-26 yang saya ikuti sebagai bagian dari misi ospek jurusan. Seluruh dokumentasi, mulai dari rangkuman materi, pengetahuan baru, hingga pendapat pribadi, disusun dalam satu file `README.md` ini.

## Tujuan Repository
- Menyimpan dan mengelola dokumentasi kegiatan workshop secara online.
- Mencatat materi dan pengetahuan baru secara terstruktur.
- Berlatih membuat repository publik di GitHub dan menggunakan `README.md` sebagai dokumentasi utama.

## Dokumentasi Kegiatan Workshop
Kegiatan yang didokumentasikan adalah **Day 1 Proyek Workshop-26** dengan materi *From AI to GitHub*, yang membahas prompt engineering, Git dan GitHub, setup Git, serta praktik membuat aplikasi sederhana. Dokumentasi mencakup tiga bagian di bawah ini: rangkuman materi, poin penting dan pengetahuan baru, serta pendapat pribadi.

---

## Rangkuman Materi
### Topik 1: Prompt Engineering

**Pengertian.** Prompt engineering adalah cara merancang instruksi agar AI memberikan jawaban yang tepat, relevan, dan layak digunakan. Prompt adalah instruksi atau masukan yang diberikan kepada model untuk mendapatkan hasil tertentu. Bentuknya bisa pertanyaan sederhana, kata kunci, instruksi rumit, atau potongan kode.

**Context is key.** Prompt singkat seperti "Create student task planner" menghasilkan jawaban yang umum. Prompt yang disertai konteks (tujuan, kebutuhan, batasan) menghasilkan jawaban yang jauh lebih sesuai.

**Struktur prompt yang baik:**

| Komponen | Fungsi |
|---|---|
| Role | Menentukan peran AI dan situasinya |
| Task | Tujuan atau tugas yang diminta |
| Context | Kebutuhan (requirements) dan batasan (constraints) |
| Format | Bentuk output yang diinginkan |

**Contoh dari materi.** Prompt untuk membuat *student task planner* berupa aplikasi web sederhana. Prompt-nya berisi goal, requirements (daftar tugas, status selesai, filter), constraints (HTML, CSS, vanilla JavaScript, tanpa library tambahan), output (kode lengkap per file, cara menjalankan, cara menguji), dan pengingat agar AI tidak mengklaim aplikasi berfungsi sebelum perilakunya diverifikasi.

**Taktik menulis prompt** (sumber: Google Cloud):
- Gunakan kata kerja aksi untuk menentukan tindakan yang diinginkan.
- Tentukan panjang dan format output.
- Tentukan target audiens.
- Sertakan fakta dan data yang relevan.
- Rujuk sumber atau dokumen tertentu.
- Definisikan istilah atau konsep kunci.

**Keuntungan prompt engineering:** meningkatkan performa model AI, mengurangi bias dan respon yang offensive, meningkatkan kontrol dan prediktabilitas, serta memberikan pengalaman yang lebih baik.

### Topik 2: Git dan GitHub

**Git** adalah version control system yang melacak siapa, kapan, dan apa saja yang diubah dalam suatu file. Git diciptakan oleh Linus Torvalds pada tahun 2005. Git adalah sistem version control terdistribusi (DVCS) yang bekerja secara lokal.

**GitHub** adalah platform berbasis web untuk menyimpan repository Git secara online dan mendukung kolaborasi.

**Alur kerja Git:**
- **Working directory:** salinan satu versi proyek yang sedang dikerjakan di komputer.
- **Staging area (index):** tempat menyimpan informasi perubahan yang akan masuk ke commit berikutnya.
- **Git directory (repository):** tempat Git menyimpan metadata dan object database proyek. Bagian inilah yang disalin saat melakukan clone.

**Perintah dasar Git:**
```bash
git init                      # memulai repo baru
git add .                     # memindahkan file ke staging area
git commit -m "pesan"         # menyimpan perubahan ke repository
```

**Perintah menghubungkan Git ke GitHub:**
```bash
git remote add <name> <url>   # menghubungkan repo lokal dengan remote
git push origin main          # mengirim branch saat ini ke remote
git pull origin main          # mengambil perubahan lalu menggabungkannya
```

**Variasi `git add`:** `git add --all` dan `git add -A` berfungsi sama (semua perubahan di repo). `git add .` menambahkan semua file di repo beserta isinya. `git add *` menambahkan file baru atau yang dimodifikasi, tetapi tidak file yang dihapus.

### Topik 3: Setup Git, VS Code, dan SSH

1. **Install Git**, lalu cek dengan `git --version`.
2. **Atur identitas Git:**
   ```bash
   git config --global user.name "Nama Kamu"
   git config --global user.email "emailkamu@example.com"
   git config --global --list
   ```
3. **Install VS Code**, lalu pasang perintah `code` di PATH (Ctrl/Cmd+Shift+P, pilih *Shell Command: Install 'code' command in PATH*) dan cek dengan `code --version`.
4. **Menambahkan repository ke Git:** dengan `git init`, atau membuat repo baru di GitHub lalu `git clone "url"` (URL diambil dari tombol *Code*).
5. **Membuat SSH key:** `ssh-keygen -t ed25519 -C "email@domain.com"`, tekan Enter untuk lokasi default, lalu isi passphrase (atau Enter dua kali tanpa passphrase). Ed25519 adalah skema tanda tangan kurva eliptik yang aman dan cepat.
6. **Menambahkan key ke SSH agent**, lalu menyalin public key (`.pub`) ke GitHub lewat *Settings → SSH and GPG keys → New SSH key*.
7. **Verifikasi koneksi:** `ssh -T git@github.com`. Jika berhasil, muncul pesan bahwa autentikasi sukses, tetapi GitHub tidak menyediakan shell access.

### Topik 4: Praktik – Student Task Planner

Peserta membuat aplikasi sederhana dengan alur:
1. Install platform AI (Claude, Antigravity, ChatGPT).
2. Tulis prompt untuk membuat web/aplikasi.
3. Tambahkan ke Git dengan `git init`.
4. Commit dan push ke GitHub.
5. Lakukan perubahan.
6. Commit dan push lagi.

---

## Poin Penting dan Pengetahuan Baru

### Pengetahuan baru yang saya dapat
- **Prompt yang spesifik menghasilkan jawaban yang lebih baik.** Struktur Role, Task, Context, dan Format membantu AI memahami apa yang saya mau.
- **Git dan GitHub itu berbeda.** Git adalah alat version control yang bekerja di komputer (lokal), sedangkan GitHub adalah platform online untuk menyimpan repository dan berkolaborasi.
- **Git punya tiga area kerja:** working directory, staging area, dan repository (.git). File harus melewati `git add` sebelum bisa di-`commit`.
- **Alur dasar kerja:** `git init` → `git add` → `git commit` → `git push`.
- **Commit adalah catatan perubahan.** Git mencatat siapa yang mengubah, kapan, dan apa yang berubah.
- **SSH key** membuat koneksi ke GitHub lebih praktis dan aman karena tidak perlu memasukkan password setiap kali push.

### Istilah baru

| Istilah | Arti singkat |
|---|---|
| Prompt | Instruksi atau masukan untuk model AI |
| Prompt engineering | Cara merancang prompt agar hasil AI tepat dan relevan |
| Version control | Pelacakan perubahan file dari waktu ke waktu |
| Repository | Tempat penyimpanan proyek beserta riwayat perubahannya |
| Commit | Penyimpanan satu set perubahan ke repository |
| Staging area | Area persiapan sebelum perubahan di-commit |
| Clone | Menyalin repository dari GitHub ke komputer |
| Push / Pull | Mengirim perubahan ke GitHub / mengambil perubahan dari GitHub |
| SSH key | Pasangan kunci untuk autentikasi ke GitHub |
| Branch | Cabang pengembangan terpisah dalam satu repository |
| Pull request | Permintaan untuk menggabungkan perubahan dari satu branch ke branch lain |

*Catatan: branch dan pull request termasuk capaian materi. Definisinya di atas saya tulis dari pemahaman dasar saya.*

### Hal yang sebelumnya belum saya ketahui
- AI tidak otomatis memberi hasil bagus. Kualitas hasilnya sangat bergantung pada kualitas prompt.
- Langkah SSH key di slide memakai macOS Keychain, jadi pengguna Windows/Linux perlu menyesuaikan langkahnya.
- Ada perintah `git add` dengan perilaku yang sedikit berbeda (`-A`, `.`, dan `*`).

### Hal yang akan saya coba setelah ini
- Menulis prompt dengan struktur Role, Task, Context, dan Format.
- Membiasakan commit dengan pesan yang jelas setiap selesai mengerjakan sesuatu.
- Memakai GitHub untuk menyimpan tugas-tugas kuliah.

---

## Pendapat Pribadi

**Kesan saya.** Workshop Day 1 ini menarik karena menghubungkan dua hal yang dekat dengan dunia kuliah dan teknologi, yaitu AI dan GitHub. Sebelumnya saya mengira AI cukup diberi perintah singkat, ternyata cara menulis prompt sangat memengaruhi hasilnya. [sesuaikan dengan kesanmu]

**Bagian yang paling bermanfaat.** Materi struktur prompt (Role, Task, Context, Format) dan alur dasar Git (`init`, `add`, `commit`, `push`). Contoh *Student Task Planner* membantu saya melihat bagaimana prompt yang jelas dan version control dipakai dalam satu proyek nyata. [sesuaikan]

**Kesulitan yang dialami.** Bagian yang paling menantang adalah setup awal, terutama konfigurasi SSH key dan memahami perbedaan working directory, staging area, dan repository. Banyak istilah baru yang perlu dibiasakan. [sesuaikan dengan kesulitan yang kamu alami]

**Manfaat untuk perkuliahan.** Git dan GitHub akan berguna untuk menyimpan tugas, mengerjakan proyek kelompok, dan membangun portofolio. Kemampuan menulis prompt yang baik juga membantu saya memakai AI sebagai alat belajar, bukan hanya mencari jawaban cepat.

**Harapan untuk hari berikutnya.** Saya berharap bisa lebih banyak praktik langsung, termasuk membuat branch dan pull request, serta mendapat contoh kolaborasi dalam satu repository bersama teman.

# OverTheWire_Write-up

![Status](https://img.shields.io/badge/Status-Ongoing-brightgreen)

[![Community](https://img.shields.io/badge/Community-Discord-blue)](https://discord.gg/CPDYM3G)

Dalam repo ini merupakan hasil dari saya mengerjakan CTF pada platform yang mungkin kalian beberapa ada yang sudah tau. OverTheWIre adalah platform CTF gratis yang menyediakan **"wargames"** berbasis terminal untuk mempelajari keamanan siber (cybersecurity) dan perintah Linux secara praktis. . Ini merupakan sarana populer bagi pemula untuk belajar peretasan etis, administrasi sistem, dan konsep jaringan melalui skenario permainan yang bertingkat, mulai dari tingkat dasar (seperti permainan "Bandit") hingga yang lebih lanjut.

![image](https://unencrypted.vercel.app/images/OverTheWire/OverTheWire.png)

## Latar Belakang

Adanya **OverTheWire (OTW)** berakar pada kebutuhan akan platform belajar keamanan siber yang bersifat praktis, gratis, dan dapat diakses oleh siapa saja. Platform ini dikembangkan oleh sebuah komunitas yang telah aktif sejak sekitar tahun 1998 untuk menyediakan lingkungan belajar yang aman dan legal bagi para peminat teknologi.

Beberapa alasan utama yang melatarbelakangi terciptanya OverTheWire adalah:

- **Pendidikan Berbasis Praktik (Learning by Doing):** OTW dibuat untuk mengatasi kejenuhan terhadap pembelajaran pasif (teori). Platform ini memungkinkan pengguna belajar langsung di server asli melalui terminal, yang jauh lebih efektif daripada sekadar membaca tutorial.
- **Fondasi untuk Pemula:** Banyak pendatang baru di dunia IT dan keamanan siber yang tidak memiliki keterampilan dasar Linux. Game seperti Bandit dirancang khusus untuk membangun fondasi kuat dalam penggunaan baris perintah (command line), navigasi file, dan konsep jaringan sebelum mereka beralih ke tantangan yang lebih kompleks.
- **Demokratisasi Pengetahuan Keamanan:** Sejak awal, OTW berkomitmen menjadi sumber daya gratis agar setiap orang—baik siswa maupun profesional—memiliki kesempatan yang sama untuk melatih "keterampilan peretasan elit" tanpa hambatan biaya.
- **Budaya Wargaming:** Platform ini membawa tradisi simulasi strategi militer ke dunia digital. Melalui skenario Capture The Flag (CTF) yang bertahap, OTW membantu pengguna mengasah kemampuan berpikir kritis, pemecahan masalah, dan ketahanan di bawah tekanan dalam lingkungan yang terstruktur.

## Tujuan Utama

- **Membangun Kemandirian Riset:** Melatih pengguna agar terbiasa mencari solusi sendiri (self-learning). Tantangannya sengaja dibuat minim instruksi agar pemain belajar cara riset, membaca dokumentasi (man pages), dan berpikir kritis layaknya seorang hacker profesional.
- **Penguasaan Command Line (Terminal):** Memastikan pengguna benar-benar mahir menggunakan baris perintah Linux. OTW percaya bahwa terminal adalah alat paling kuat dalam keamanan siber, dan melalui permainan ini, pengguna dipaksa untuk tidak bergantung pada antarmuka visual (GUI).
- **Memahami Kerentanan Secara Teknis:** Membantu pengguna memahami bagaimana sebuah sistem bisa ditembus dengan cara mempraktikkannya langsung, bukan hanya teori. Ini mencakup pemahaman tentang izin file, enkripsi, eksploitasi kode, hingga jaringan.
- **Menyediakan Jalur Belajar yang Terstruktur:** Lewat level yang bertahap (dari Bandit hingga Vortex atau Drifter), OTW memberikan kurikulum belajar yang jelas dari tingkat pemula hingga tingkat lanjut bagi komunitas keamanan global secara gratis.

## Wargames

OverTheWire (OTW) menawarkan berbagai permainan (wargames) yang dirancang secara progresif. Setiap permainan memiliki fokus materi yang berbeda, sehingga kamu bisa memilih sesuai dengan topik keamanan siber yang ingin kamu pelajari.

Berikut adalah daftar permainan utama di OverTheWire beserta fokus materinya:

- **Bandit (Dasar Linux):** Gerbang utama bagi pemula. Fokus pada perintah dasar terminal, navigasi sistem file, dan penggunaan tools Linux dasar.
- **Natas (Keamanan Web):** Mengajarkan kerentanan pada aplikasi web sisi server (server-side), seperti manipulasi header, eksploitasi kode PHP, dan keamanan basis data.
- **Leviathan (Analisis Biner Dasar):** Mengenalkan cara mencari kerentanan dalam program biner dan melakukan reverse engineering sederhana.
- **Krypton (Kriptografi):** Fokus pada pemecahan kode dan sandi, mulai dari sandi klasik seperti Caesar dan Vigenere hingga konsep kriptografi modern.
- **Narnia (Eksploitasi Biner):** Belajar tentang buffer overflows dan bagaimana mengeksploitasi kelemahan dalam kode untuk mendapatkan akses sistem.
- **Behemoth, Utumno, Maze (Eksploitasi Lanjutan):** Permainan ini merupakan kelanjutan dari Narnia dengan tingkat kesulitan yang jauh lebih tinggi dalam hal peretasan biner dan memori.
- **Vortex, Drifter (Keamanan Jaringan & Sistem):** Fokus pada eksploitasi tingkat lanjut yang melibatkan interaksi jaringan dan sistem yang lebih kompleks.

## Persyaratan Teknis-nya

### Sistem Operasi (OS)

Sebenarnya kamu bisa menggunakan sistem operasi apa saja, asalkan memiliki aplikasi terminal untuk menjalankan perintah teks.

- **Linux / macOS:** Sudah memiliki terminal bawaan yang sangat optimal.
- **Windows:** Kamu bisa menggunakan PowerShell, Command Prompt (Windows 10/11), atau menginstal Windows Subsystem for Linux (WSL) untuk pengalaman Linux yang asli.
- Kalau masih bingung, saya pribadi menggunakan GitBash yang command-nya sebagian sudah mirip dengan yang ada pada Linux.

### Aplikasi SSH Client

Semua permainan di OverTheWire diakses menggunakan protokol `SSH` (Secure Shell).

![image](https://repository-images.githubusercontent.com/477310984/dc086718-5c72-4fc5-87cb-7e23280f197e)

- **Terminal Bawaan:** Pada Linux, macOS, dan Windows 10/11 terbaru, kamu cukup membuka terminal dan mengetik perintah `ssh`.
- **Aplikasi Pihak Ketiga (Opsional):** Jika kamu menggunakan Windows versi lama atau ingin antarmuka yang lebih lengkap, kamu bisa mengunduh PuTTY atau MobaXterm.

### Koneksi Internet

Koneksi internet yang stabil sangat dibutuhkan untuk menjaga sesi SSH kamu tidak terputus *(timeout)* saat sedang mengetik perintah di server.

## The Rules

### 1. Dilarang Berbagi Password/Flag (No Spoilers)

Ini adalah aturan yang paling krusial. Kamu dilarang keras membagikan kata sandi (password) untuk level mana pun di tempat umum (forum, komentar YouTube, atau blog). Tujuannya agar orang lain benar-benar belajar melalui proses berpikir mereka sendiri, bukan sekadar copy-paste.

### 2. Kebijakan "Walkthrough"

Jika kamu membuat konten (blog/video) tentang cara menyelesaikan sebuah level, OTW menyarankan:

- **Jelaskan prosesnya:** Fokuslah pada metode, perintah yang digunakan, dan logika di baliknya.
- **Jangan sertakan password:** Biarkan pembaca/penonton menjalankan perintah tersebut sendiri untuk mendapatkan password mereka.

### 3. Jangan Menyerang Infrastruktur OTW

**Ingat**, tantangan ini ada di server mereka. Kamu dilarang melakukan serangan *Denial of Service (DoS)*, mencoba merusak server, atau mencari celah keamanan di platform OTW itu sendiri (kecuali itu memang bagian dari instruksi level tersebut). Gunakan teknik peretasan hanya pada target yang sudah ditentukan.

### 4. Hormati Pengguna Lain

Server OTW digunakan secara bersama-sama oleh ribuan orang dari seluruh dunia.

- Jangan mencoba mengintip atau mengganggu sesi SSH pengguna lain.
- Jangan mengubah file sistem atau melakukan tindakan yang bisa membuat server menjadi lambat/berhenti bekerja bagi orang lain.

### 5. Terakhir... Budayakan "RTFM" (Read The F***ing Manual)

Dalam komunitas OTW, ada budaya kuat untuk membaca dokumentasi sebelum bertanya. Jika kamu merasa diposisi "mentok", sangat disarankan untuk mencari tahu lewat perintah man (manual) di Linux atau riset di Google terlebih dahulu sambil minum kopi sebelum meminta bantuan di komunitas.

## Perbedaan-nya dengan platform lain?

| Fitur | OverTheWire | TryHackMe | HackTheBox |
| --- | --- | --- | --- |
| **Target Pengguna** | Benar-benar pemula (dari nol). | Pemula hingga Menengah. | Menengah hingga Profesional. |
| **Metode Belajar** | Terminal-only. Langsung praktik di server via SSH. | Tutorial interaktif. Ada modul bacaan dan pertanyaan. | Skenario nyata. Fokus pada penetrasi mesin/server utuh. |
| **Fokus Utama** | Dasar Linux, baris perintah, dan logika sistem. | Berbagai alat (tools) dan konsep keamanan populer. | Eksploitasi kreatif dan teknik peretasan tingkat lanjut. |
| **Biaya** | **100% Gratis** selamanya. | Gratis (dengan opsi langganan premium). | Gratis (dengan opsi langganan untuk mesin lama). |
| **Antarmuka** | Minimalis (Hanya teks di situs web). | Sangat visual, ada dashboard dan progres belajar. | Visual dan kompetitif (ada sistem ranking). |

### Kapan Kamu Harus Menggunakan Masing-masing?

- **Pilih OverTheWire jika:** Kamu ingin memperkuat fondasi Linux dan ingin belajar "cara keras" tanpa bantuan instruksi visual. OTW akan membuat kamu sangat mahir menggunakan terminal.
- **Pilih TryHackMe jika:** Kamu baru mulai dan butuh bimbingan terstruktur yang menjelaskan teori sebelum praktik. Sangat cocok untuk memahami konsep seperti Networking atau Web App Sec.
- **Pilih Hack The Box jika:** Kamu sudah paham dasar-dasar peretasan dan ingin menguji kemampuanmu melawan mesin yang memiliki tingkat kesulitan seperti dunia nyata.

**Kesimpulannya:** Kebanyakan orang memulai dari OverTheWire (Bandit) untuk menguasai terminal, lalu pindah ke TryHackMe untuk belajar konsep luas, dan akhirnya ke Hack The Box untuk asah skill profesional.

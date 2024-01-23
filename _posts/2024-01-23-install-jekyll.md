---
layout: post
title:  "install jekyll!"
date:   2024-01-23 12:04:54 +0800
categories: jekyll update
---
Berikut adalah langkah-langkah untuk menginstal Jekyll di lingkungan Windows:

1. Instal Ruby:
Unduh RubyInstaller untuk Windows dari rubyinstaller.org.
Pada halaman unduhan, pilih versi Ruby terbaru (biasanya versi stabil). Pilih opsi "Ruby+Devkit" saat mengunduh.
Jalankan installer yang diunduh dan ikuti petunjuk instalasi.
Pastikan untuk memilih opsi "MSYS2" dan menambahkan Ruby ke PATH selama proses instalasi.
2. Verifikasi Instalasi Ruby:
Buka Command Prompt (CMD) dan jalankan perintah:

bash
Copy code
ruby -v
Jika Anda melihat versi Ruby yang diinstal, itu berarti instalasi Ruby berhasil.

3. Instal Jekyll:
Setelah Ruby terinstal, buka Command Prompt dan jalankan perintah berikut untuk menginstal Jekyll:
bash
Copy code
gem install jekyll bundler
Setelah proses selesai, verifikasi instalasi dengan menjalankan perintah:
bash
Copy code
jekyll -v
4. Buat dan Jalankan Proyek Jekyll Baru:
Buat proyek Jekyll baru dengan perintah:
bash
Copy code
jekyll new nama-situs
Pergi ke direktori proyek:
bash
Copy code
cd nama-situs
5. Jalankan Server Lokal (Opsional):
Jalankan server lokal untuk melihat situs Anda sebelum menerapkannya di hosting. Di dalam direktori proyek, jalankan perintah:

bash
Copy code
bundle exec jekyll serve
Buka browser dan kunjungi http://localhost:4000 untuk melihat situs lokal Anda.

Sekarang, Anda telah berhasil menginstal Jekyll di lingkungan Windows dan membuat proyek Jekyll baru. Pastikan untuk membaca dokumentasi resmi Jekyll (https://jekyllrb.com/) untuk informasi lebih lanjut tentang cara menggunakan dan menyesuaikan situs Jekyll Anda.



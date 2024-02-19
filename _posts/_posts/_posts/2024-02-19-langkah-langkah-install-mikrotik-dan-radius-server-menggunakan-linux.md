# Instalasi MikroTik RouterOS dan FreeRADIUS di Linux adalah proses yang melibatkan beberapa langkah. Di bawah ini adalah langkah-langkahnya:

## 1. Instalasi MikroTik RouterOS:
a. Unduh ISO RouterOS:
- Kunjungi situs resmi MikroTik dan unduh file ISO RouterOS.
- Pastikan untuk memilih versi yang sesuai dengan arsitektur perangkat keras Anda (x86, x64, ARM, dll.).

b. Persiapkan USB Flash Drive (Opsional):
- Jika Anda ingin menginstal RouterOS pada perangkat keras fisik, siapkan USB flash drive dan format menjadi sistem berkas yang sesuai dengan instruksi MikroTik.

c. Boot dari ISO:
- Boot perangkat Anda dari ISO yang sudah Anda unduh tadi. Pastikan pengaturan boot pada perangkat Anda sudah diatur untuk mem-boot dari USB atau DVD, sesuai dengan perangkat keras Anda.

d. Ikuti Proses Instalasi:
- Ikuti petunjuk instalasi yang muncul di layar.
- Pilih drive atau media penyimpanan yang sesuai untuk menginstal RouterOS.
- Lanjutkan dengan konfigurasi jaringan dan konfigurasi awal lainnya sesuai dengan kebutuhan Anda.

## 2. Instalasi FreeRADIUS Server:
a. Instalasi Paket FreeRADIUS:
- Buka terminal di sistem Linux Anda.
- Jalankan perintah untuk menginstal paket FreeRADIUS dari repositori sistem operasi Anda. Misalnya, untuk Ubuntu, Anda dapat menggunakan perintah:
- sudo apt-get update
- sudo apt-get install freeradius
  
b. Konfigurasi FreeRADIUS:
- Konfigurasi utama FreeRADIUS ada di dalam direktori /etc/freeradius/.
- Konfigurasikan file clients.conf untuk menambahkan konfigurasi perangkat MikroTik sebagai klien RADIUS.
- Konfigurasikan file users untuk menambahkan pengguna dan kata sandi RADIUS.
- Sesuaikan konfigurasi sesuai dengan kebutuhan jaringan Anda.
  
c. Mulai Layanan FreeRADIUS:
- Setelah konfigurasi selesai, mulai layanan FreeRADIUS menggunakan perintah:
- sudo systemctl start freeradius
  
d. Verifikasi Layanan FreeRADIUS:
- Gunakan perintah berikut untuk memeriksa apakah layanan FreeRADIUS berjalan dengan baik:
- sudo systemctl status freeradius
  
## 3. Konfigurasi MikroTik RouterOS untuk Menggunakan FreeRADIUS:
- Masuk ke antarmuka administrasi MikroTik menggunakan browser web atau melalui koneksi terminal.
- Konfigurasi RADIUS server pada MikroTik dengan menentukan alamat IP dan kata sandi yang sesuai dengan server FreeRADIUS yang telah Anda konfigurasi.
  
Dengan langkah-langkah di atas, Anda telah berhasil menginstal MikroTik RouterOS dan FreeRADIUS Server di sistem Linux Anda. Pastikan untuk memeriksa dokumentasi resmi dari MikroTik dan FreeRADIUS untuk konfigurasi lebih lanjut dan penyesuaian yang mungkin diperlukan.







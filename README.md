# Bismillahirrahmanirrahim

## Janji
Saya Muhammad Naufal Arbanin dengan NIM 2310850 mengerjakan soal Tugas Praktikum 9 dalam mata kuliah Desain Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Penjelasan Alur
### 1. Tambah Mahasiswa (Create)
Alur:
- User buka form tambah (form_add.php).

- Isi form: NIM, Nama, Tempat Lahir, Tanggal Lahir, Gender, Email, No Telp.

- Saat klik tombol "Tambah", form dikirim ke index_request.php dengan method="post" dan parameter aksi=add.

- Di index_request.php, aksi ini akan memanggil fungsi untuk menambahkan data ke database (tabel students) menggunakan kelas presenter (misal: ProsesMahasiswa->tambahData()).

- Setelah sukses, halaman redirect ke halaman daftar mahasiswa (index.php).

### 2. Tampilkan Mahasiswa (Read)
Alur:
- Halaman index.php akan memanggil ProsesMahasiswa.php.

- Di dalamnya, ada method prosesDataMahasiswa() yang mengambil semua data dari tabel students dan menyimpannya dalam array/variabel presenter.

- Data ditampilkan dalam bentuk tabel dengan kolom: NIM, Nama, Tempat, Tanggal Lahir, Gender, Email, Telp.

- Tabel ini juga menyertakan tombol Edit dan Hapus.

### 3. Edit Mahasiswa (Update)
Alur:
- Di halaman daftar mahasiswa (index.php), user klik tombol Edit di salah satu baris.

- Halaman diarahkan ke form_edit.php?id=X, di mana X adalah id mahasiswa.

- Di form_edit.php, program:

  - Memanggil ProsesMahasiswa → prosesDataMahasiswa()

  - Mencari data berdasarkan id

  - Menampilkan form dengan data yang sudah terisi

- Setelah user mengubah data dan klik "Simpan Perubahan", form mengirim data ke index_request.php dengan aksi=edit.

- Di index_request.php, sistem memanggil method untuk update data mahasiswa di database berdasarkan id.

- Redirect kembali ke halaman daftar mahasiswa.

### 4. Hapus Mahasiswa (Delete)
Alur:
- User klik tombol Delete di tabel student_index.php.

- Link mengarah ke index_request.php?aksi=delete&id=X.

- Akan muncul konfirmasi JavaScript (bisa pakai confirm()).

- Jika user setuju, index_request.php akan memanggil method untuk menghapus data dari tabel students berdasarkan id.

- Redirect kembali ke halaman utama dengan data terbaru.

  
File index_request.php berfungsi sebagai controller utama yang menangani permintaan (request) dari form input di aplikasi CRUD Mahasiswa. File ini menjadi penghubung antara tampilan (form) dan proses bisnis (presenter), serta menangani aksi seperti tambah, edit, dan hapus data.

## Dokumentasi Video
https://github.com/user-attachments/assets/8489c835-3a0f-4200-a91b-3c4bda549121

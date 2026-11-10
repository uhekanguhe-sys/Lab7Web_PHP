1.Menjalankan PHP, membuat index.php yang diakses melalui browser localhost
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/46c8b898-22eb-4d1f-b3fd-61fc7a618b66" />
2.Membuat variabel, operator dan percabangan.
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/1553a419-0e62-4acc-9fbf-9b730d8cf237" />
Ubah nilai Tugas menjadi 95, nilai UTS menjadi 85 dan nilai UAS menjadi 85. Hasilnya
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/64828555-4ffc-49b9-aaa0-4853cce0fcbd" />
3.Perulangan dan aray. 
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/9ae6b839-8dc6-4f03-9e35-05c201d8e354" />
Tambahkan lagi 3 nama ( “indra”, “Yana”, “Bagong”)
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/6deb9f06-d5a1-4d17-824f-d91d45e3a75a" />
4.Membuat Fungtion:
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/72805f58-ce1f-422a-93d6-09aa05e482bd" />
5.Memproses form dengan GET
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/6af29245-14db-4d54-830b-5840e2c5000c" />
6.Memproses form dengan POST.
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/843892f8-e66f-441e-9420-e9074eaef10c" />
Pengujian dengan data lengkap
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/6154f3e9-1c94-4f47-9fb8-a79118d57496" />
7.Pengolahan data sederhana, misal input Nama barang : Barang, Harga  150000, Jumlah : 9. hasilnya adalah 1350000.
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/cbdeb8cd-caa8-45f8-83e1-4f9d6bfc4b75" />
Uji dengan jumlah desimal dan harga negatif.
Hasilnya muncul peringatan “Value must be greater than or equal to 1.” (Nilai harus lebih besar atau sama dengan 1)
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/f105f8f1-a600-4f64-aaf4-9f411abeb19c" />

Mini project. 
<img width="692" height="432" alt="image" src="https://github.com/user-attachments/assets/111d4a86-6f71-4897-8277-c4c41712dc0d" />
Pemisahan proses dan tampilan: semua validasi ada di blok PHP paling atas, sedangkan HTML di bawah hanya menampilkan hasilnya lewat if ($error) dan if ($data).
Semua error tampil: foreach ($error as $pesan) mencetak semua pesan kesalahan sekaligus.
Ringkasan data: hanya muncul jika $data terisi, yaitu saat array $error kosong.
htmlspecialchars(): dipakai lewat fungsi e() pada setiap data yang ditampilkan, termasuk isi kolom form.
Isi form dipertahankan: value="<?= e($_POST["nama"] ?? "") ?>" membuat isian tidak hilang ketika ada error, sehingga pengguna tidak perlu mengetik ulang.
Kolom form memakai type="text" tanpa required: supaya validasi server-side terlihat bekerja saat diuji. Kalau mau, kamu bisa menambah required untuk validasi tambahan di browser, tetapi validasi server tetap wajib.

Skenario uji

Kosongkan semua kolom lalu kirim: muncul semua pesan error.
Isi semester 20 atau abc: muncul pesan semester.
Isi email siti@ : muncul pesan format email.
Isi semua dengan benar, misalnya semester 3 dan email siti@mail.com: muncul ringkasan data.
Isi nama dengan <b>Siti</b>: tampil sebagai teks biasa, bukan huruf tebal (bukti htmlspecialchars() bekerja).

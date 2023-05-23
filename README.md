## **Tugas Praktikum**

### !. Lakukan penambahan data pada table mahasiswa dengan mengisi kd_ds yang belum ada pada data dosen

![1](foto/a1.png)

### 2. Hapus satu record data pada table dosen yang telah dirujuk pada tabel mahasiswa

![2](foto/a2.png)

### 3. Ubah mode menjadi ON UPDATE CASCADE ON DELETE RESTRICT

![3](foto/a3-6.png)

### 4. Lakukan perubahan data pada table dosen kd_ds

![4](foto/a4.png)

### 5. Lakukan penghapusan data pada table dosen

![5](foto/a5.png)

### 6. Ubah mode menjadi ON UPDATE CASCADE ON DELETE SET NULL

![6](foto/a3-6.png)

###  7. Lakukan penghapusan data pada table dosen



## Evaluasi dan Pertanyaan

### 1. Apa bedanya penggunaan RESTRICT dan penggunaan CASCADE

Penggunaan RESTRICT dan CASCADE adalah dua opsi yang tersedia dalam basis data untuk mengatur tindakan yang diambil terkait integritas referensial saat terjadi perubahan atau penghapusan data dalam tabel yang memiliki hubungan referensial dengan tabel lain. Berikut adalah perbedaan antara keduanya:

RESTRICT: 
Ketika opsi RESTRICT digunakan, itu berarti basis data akan menghentikan operasi yang akan melarang integritas referensial. Jika ada hubungan referensial antara dua tabel dan Anda mencoba menghapus atau memodifikasi data yang akan melanggar hubungan referensial tersebut, operasi tersebut akan gagal dan menghasilkan pesan kesalahan. Dalam konteks penghapusan data, jika ada entri yang dikaitkan dengan entri lain dalam tabel yang berhubungan, pemusnahan akan dihentikan.

CASCADE:
Ketika opsi CASCADE digunakan, berarti basis data akan mengambil tindakan tambahan untuk menjaga integritas referensial dengan melakukan tindakan yang sama pada tabel terkait. Jadi, jika ada hubungan referensial antara dua tabel dan Anda menghapus atau memodifikasi data dalam tabel yang memiliki referensi, operasi tersebut akan berdampak pada tabel terkait juga.

Penghapusan CASCADE: Jika Anda menghapus baris dari tabel utama, penghapusan CASCADE akan menghapus semua baris yang terkait di tabel terkait juga. Misalnya, jika Anda memiliki tabel "Kategori" dan tabel "Produk", dan ada hubungan referensi antara kolom "kategori_id" dalam tabel "Produk" dengan kolom "id" dalam tabel "Kategori", jika Anda menghapus sebuah kategori, semua produk yang terkait dengan kategori tersebut juga akan dihapus secara otomatis.
Pembaruan CASCADE: Jika Anda memperbarui nilai kolom yang digunakan dalam hubungan referensial pada tabel utama, pembaruan CASCADE akan memperbarui nilai-nilai yang sesuai di tabel terkait juga.
Penggunaan CASCADE harus dilakukan dengan hati-hati karena tindakan ini dapat berdampak luas dan menghapus atau memodifikasi banyak data secara otomatis. Oleh karena itu, perlu dipertimbangkan dengan cermat sebelum menggunakannya.

Inti dari perbedaan antara RESTRICT dan CASCADE adalah bahwa RESTRICT menghentikan operasi yang melanggar integritas referensial, sedangkan CASCADE melanjutkan operasi dengan mengambil tindakan pada tabel terkait untuk menjaga integritas referensial. Pilihan antara RESTRICT dan CASCADE tergantung pada kebutuhan dan desain aplikasi basis data yang sedang digunakan.
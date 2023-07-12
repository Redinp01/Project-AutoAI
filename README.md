# IMPLEMENTATION GENERATE PYTHON NOTEBOOK FOR PIPELINE MODELS USING AUTOAI AND USE DATASET HUMAN RESOURCES IN SALARY

1. Jalankan eksperiment AutoAI

![Screenshot 2023-07-12 125653](https://github.com/Redinp01/Project-AutoAI/assets/139215726/68ecb861-d227-4ed5-a311-d867ac70df56)

2.	Buka proyek yang dibuat di Watson Studio. Klik Add ke Proyek. Klik tombol "+" di pojok kanan atas lalu klik "Eksperimen AutoAI".
3.	Beri nama eksperimen (Analisis eaa), sambungkan layanan Watson Machine Learning menggunakan menu drop-down dan klik Buat.
4.	Di layer Tambahkan sumber data, klik Select from project dan periksa human_resources. csv dan klik Select asset.
5.	Di bawah bagian Konfigurasi detail, klik Tarik what do you want to predict? Cari dan pilih result dari daftar. Jika anda menggunakan kumpulan data yang berbeda, pilih kolom tempat anda ingin AutoAI menjalankan prediksi.Klik Run Experiment di sebelah kanan bawah.

Anda akan melihat notifikasi yang menunjukkan eksperimen AutoAI telah dimulai. Bergantung pada ukuran kumpulan data, langkah ini akan memakan waktu beberapa menit untuk diselesaikan

![Screenshot 2023-07-12 130100](https://github.com/Redinp01/Project-AutoAI/assets/139215726/3f415376-b7ab-48d1-8976-d164035e99d9)

6. Buat buku catatan tingkat percobaan.

![Screenshot 2023-07-12 130300](https://github.com/Redinp01/Project-AutoAI/assets/139215726/4a87f757-f0d9-4368-82d1-01488f5c1b80)

Ini eksperiment notebook yang menyediakan kode beranotasi sehingga anda dapat:
•	Berinteraksi dengan pipeline model terlatih
•	Mengakses detail model secara terprogram (termasuk kepentingan fitur dan metrik pembelajaran mesin)
•	Visualisasikan setiap pipa sebagai grafik, dengan setiap node
•	didokumentasikan, untuk memberikan transparansi
•	Download pipeline yang dipilih dan uji secara lokal
•	Buat penerapan dan nilai modelnya
•	Dapatkan konfigurasi eksperimen, yang dapat Anda gunakan untuk otomatisasi atau integrasi dengan aplikasi lain

Untuk membuat buku catatan eksperimen, lakukan Langkah-langkah berikut:
1. Setelah percobaan AutoAI selesai, klik Save experiment code tombol yang ditunjukkan oleh icon floppy

![Screenshot 2023-07-12 130559](https://github.com/Redinp01/Project-AutoAI/assets/139215726/8fd56312-52f7-4236-8036-84ddd625ce94)

2. Di prompt, ubah NamaSave experiment code default jika diperlukan dan klik. Munculan akan muncul yang menunjukkan bahwa notebook berhasil disimpan. Sekarang Anda akan melihat buku catatan ini di bawah bagian Buku Catatan di dalam tab Aset. Save

# Muat dan jalankan notebook
Luangkan waktu untuk melihat-lihat bagian buku catatan untuk mendapatkan ikhtisar. Buku catatan terdiri dari sel teks (penurunan harga atau judul) dan sel kode. Sel-sel penurunan harga memberikan komentar tentang apa yang dirancang untuk dilakukan oleh kode.
Anda akan menjalankan sel satu per satu dengan menyorot setiap sel, lalu klik Runtombol di bagian atas notebook atau tekan pintasan keyboard untuk menjalankan sel (Shift + Enter tetapi dapat bervariasi berdasarkan platform). Saat sel sedang berjalan, tanda bintang ([*]) akan muncul di sebelah kiri sel. Ketika sel itu selesai mengeksekusi, nomor urut akan muncul Buku catatan yang dihasilkan sudah diisi sebelumnya dengan kode Python dan dibagi menjadi 4 bagian utama sebagai berikut.

# Pengaturan
Bagian ini berisi kredensial ke Cloud Object Storage yang digunakan untuk mengambil pipeline AutoAI saat ini. Sel berisi kode yang sudah diisi sebelumnya untuk mengekstrak data pelatiha n yang digunakan untuk membuat jalur pipa dan hasil jalur pipa.

![Screenshot 2023-07-12 131240](https://github.com/Redinp01/Project-AutoAI/assets/139215726/2f664655-9048-43e1-bb7b-d91b113e7da1)

Bagian ini juga berisi metadata pipeline saat ini yang digunakan untuk menjalankan eksperimen.

![Screenshot 2023-07-12 131301](https://github.com/Redinp01/Project-AutoAI/assets/139215726/09fb5643-9c78-4511-b2fc-0d445aa9f9ea)

# API Keys
Untuk dapat mengakses instance WML, pengguna perlu membuat kunci api melalui akun cloud dan menempelkannya di sel seperti yang ditunjukkan pada sel di bawah ini. Petunjuk untuk mendapatkan kunci cloud api dijelaskan di bagian penurunan harga dari tangkapan layar yang ditunjukkan di bawah ini.

![Screenshot 2023-07-12 131844](https://github.com/Redinp01/Project-AutoAI/assets/139215726/40b2d37e-9ad6-4502-9c20-683ef8e16d79)

# Perbandingan Pipeline
Untuk membandingkan semua jalur pipa yang dihasilkan, panggil summary () metode pada objek jalur pipa. Model dengan performa terbaik disimpan di bawah best_pipeline_namevariabel

![Screenshot 2023-07-12 132019](https://github.com/Redinp01/Project-AutoAI/assets/139215726/16f77cbd-573a-453e-a697-ce1c114f6d22)

# Periksa Pipeline
Di dalam bagian notebook ini, terdapat kode untuk memvisualisasikan tahapan dalam model sebagai grafik menggunakan API AutoAI Watson Machine Learning.

![Screenshot 2023-07-12 132618](https://github.com/Redinp01/Project-AutoAI/assets/139215726/72a14a8c-3334-420f-9893-cacd78b3ae71)


Bagian ini juga berisi kode yang mengekstrak model saat ini dan mencetaknya sebagai kode Python.

![Screenshot 2023-07-12 132648](https://github.com/Redinp01/Project-AutoAI/assets/139215726/2bc3fbad-a8ac-45d4-82fd-2a5b24185e86)


# Terapkan dan skor sebagai layanan web menggunakan instans WML
Bagian notebook ini berisi kode yang menerapkan model pipeline sebagai layanan web menggunakan Watson Machine Learning. Bagian ini mengharuskan pengguna memasukkan kredensial agar dapat mengidentifikasi instans WML dan ruang penerapan yang tepat.

![Screenshot 2023-07-12 132813](https://github.com/Redinp01/Project-AutoAI/assets/139215726/f81e526a-5046-47b6-9cf2-da22c3d3c52e)


Dapatkan target_space_id seperti yang ditunjukkan pada langkah- langkah di atas dan rekatkan di dalam bagian penerapan pembuatan. Watson Machine Learning API menggunakan wml_credentialsdan target_space_id untuk menerapkan model pembelajaran mesin sebagai layanan web.

![Screenshot 2023-07-12 133731](https://github.com/Redinp01/Project-AutoAI/assets/139215726/e7d42041-f1a4-45b3-a21e-4a8c332d6181)


Setelah sel dieksekusi, model dipromosikan ke ruang penerapan dan sekarang tersedia sebagai layanan web dan dapat diverifikasi dari dalam UI seperti yang ditunjukkan di bawah ini.

![Screenshot 2023-07-12 134022](https://github.com/Redinp01/Project-AutoAI/assets/139215726/637ec044-1706-494f-895c-b885710ccbcf)


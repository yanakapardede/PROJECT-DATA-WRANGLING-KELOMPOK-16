# PROJECT-DATA-WRANGLING-KELOMPOK-15
Analisis Pengaruh Curah Hujan dan Inflasi terhadap Harga Bahan Pokok di Pulau Jawa Tahun 2024

Kelompok 15
Shafa Fatimah Az Zahra (1314623062)
Yanaka Sofia Pardede (24031554065)
Putri Sofiyatus Salwa (24031554112)

Repositori ini berisi proyek Data Wrangling dan Exploratory Data Analysis (EDA) untuk menganalisis hubungan antara curah hujan, inflasi, dan harga bahan pokok di enam provinsi Pulau Jawa sepanjang tahun 2024.
Proyek ini berfokus pada pembersihan data, standarisasi format antarprovinsi, integrasi, agregasi, transformasi, dan EDA.
Sumber Data
Curah Hujan: BMKG (data harian tahun 2024)
Inflasi: BPS (per provinsi, subkelompok makanan, minuman, dan tembakau, tahun 2024)
Harga Bahan Pokok: PIHPS (data harian → diolah menjadi bulanan per komoditas)

Deskripsi Data:
1. Curah Hujan (BMKG)
Data curah hujan diambil dari BMKG berupa 72 file harian dari enam provinsi di Pulau Jawa. Semua file per provinsi digabung terlebih dahulu, lalu dilakukan perhitungan rata-rata untuk mendapatkan nilai curah hujan bulanan. Dataset akhir berisi curah hujan bulanan terstandarisasi untuk seluruh provinsi.

2. Inflasi (BPS)
Untuk data inflasi, kami mengunduh enam file dari BPS. Empat provinsi memiliki format tabel yang sama, sedangkan dua provinsi lainnya (DKI Jakarta dan DIY) menggunakan format berbeda namun seragam satu sama lain. Karena itu dibuat dua alur pembersihan data agar struktur antarprovinsi dapat diseragamkan. Setelah struktur tabel konsisten, seluruh data inflasi dari enam provinsi digabung menjadi satu dataset inflasi Pulau Jawa tahun 2024.

3. Harga Bahan Pokok (PIHPS)
Data harga bahan pokok diperoleh dari PIHPS, di mana setiap komoditas disimpan dalam file terpisah dengan format wide. Setiap file dibersihkan, difilter hanya untuk provinsi Pulau Jawa, kemudian ditransformasikan ke format long agar dapat digabung menjadi satu dataset besar. Setelah seluruh komoditas tergabung, data dipivot kembali sehingga setiap baris mewakili satu provinsi dan bulan, dengan kolom berisi harga masing-masing komoditas.
Pada dataset PIHPS yang kami gunakan, seluruh komoditas memang sudah memakai satuan kilogram (kg) dari sumbernya. Karena itu, kami tidak perlu melakukan konversi satuan lagi. Penggunaan satuan yang sama memudahkan kami dalam membandingkan harga antar komoditas dan menganalisis datanya.
Satuan komoditasnya adalah sebagai berikut:
Beras: Kilogram (kg) 
Daging ayam: Kilogram (kg)
Daging sapi: Kilogram (kg)
Telur ayam: Kilogram (kg)
Bawang merah: Kilogram (kg)
Bawang putih: Kilogram (kg)
Cabai merah: Kilogram (kg)
Cabai rawit: Kilogram (kg)
Minyak goreng: Kilogram (kg)
Gula pasir: Kilogram (kg)

4. Integrasi Akhir Dataset
Seluruh dataset (BMKG, BPS, PIHPS) digabung menggunakan kunci:
Provinsi + Bulan
Hasilnya adalah dataset gabungan Pulau Jawa yang siap dianalisis.

5. Tahap Analisis (EDA)
Eksplorasi tren curah hujan, inflasi, dan harga bahan pokok.
Perbandingan antarprovinsi.
Visualisasi pola hubungan antar variabel menggunakan scatter plots & line charts.
Identifikasi volatilitas komoditas (cabai merah, cabai rawit, bawang merah, bawang putih, beras, daging ayam, daging sapi, telur ayam, minyak goreng, dan gula pasir)

6. Hasil yang kami peroleh:
Dataset final sudah siap digunakan untuk analisis regresi berganda.
Sudah ditemukan insight awal mengenai hubungan curah hujan, inflasi, dan harga bahan pokok.
EDA memberikan gambaran pola tren dan hubungan antarvariabel.

7. Rencana Lanjutan:
Pemodelan regresi.

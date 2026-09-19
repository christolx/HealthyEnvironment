# Proposal Further Development — LingkunganSehat

Saya ingin melanjutkan dan mengembangkan lebih lanjut project **LingkunganSehat** yang sebelumnya dibuat sebagai kegiatan Community Service. Pengembangan akan difokuskan pada peningkatan usability, reliability, serta penambahan fitur yang membantu pengemudi ojek online memahami kondisi lingkungan dan mengambil keputusan yang lebih baik saat bekerja.

## Rencana Pengembangan

### 1. Evaluasi Aplikasi Existing
Melakukan evaluasi terhadap aplikasi yang sudah ada untuk mengidentifikasi bagian yang perlu ditingkatkan, terutama pada:
- kemudahan penggunaan
- kejelasan informasi
- tampilan mobile
- reliability aplikasi
- error handling
- penyajian rekomendasi kepada pengguna

### 2. UI/UX Improvement
Melakukan perbaikan antarmuka agar aplikasi lebih mudah dan cepat dipahami saat digunakan di lapangan, meliputi:
- tampilan risk level yang lebih jelas
- layout mobile yang lebih responsif
- ukuran teks dan tombol yang lebih nyaman
- penyajian informasi lokasi dan waktu yang lebih rapi
- konsistensi penggunaan bahasa Indonesia
- penyederhanaan informasi AQI, UV, suhu, dan kondisi lingkungan
- rekomendasi yang lebih singkat, jelas, dan actionable

### 3. Dark / Light Mode Support
Melengkapi fitur pengaturan tema dengan dukungan **dark mode** dan **light mode**, sehingga pengguna dapat menyesuaikan tampilan aplikasi dengan kondisi penggunaan dan preferensi masing-masing.

Pengaturan tema akan disimpan agar tetap digunakan ketika aplikasi dibuka kembali.

### 4. Reliability Improvement
Melakukan perbaikan terhadap beberapa masalah teknis pada aplikasi, terutama:
- penanganan error saat koneksi internet bermasalah
- penanganan kegagalan location permission atau location access
- perbaikan mekanisme refresh data
- fallback yang lebih baik saat data gagal diambil
- perbaikan alur loading dan error state agar aplikasi tetap mudah dipahami pengguna

### 5. Hourly Environmental Forecast
Menambahkan fitur **hourly environmental forecast** agar pengguna dapat melihat kondisi lingkungan untuk beberapa jam ke depan, seperti:
- suhu
- kondisi cuaca
- UV Index
- indikator risiko lingkungan

Fitur ini bertujuan agar pengguna tidak hanya melihat kondisi saat ini, tetapi juga dapat memahami perubahan kondisi lingkungan dalam beberapa jam berikutnya.

### 6. Security Improvement
Melakukan peningkatan keamanan pada arsitektur aplikasi, terutama pada cara aplikasi mengakses layanan eksternal.

Perbaikan akan difokuskan pada:
- mencegah API key terekspos langsung pada frontend/client
- memindahkan credential sensitif ke server-side environment
- menggunakan backend/proxy sederhana untuk mengakses WeatherAPI
- mengurangi risiko penyalahgunaan API key dan penggunaan quota oleh pihak tidak berwenang

### 7. Lower Environmental-Risk Time Recommendation
Mengembangkan fitur rekomendasi waktu berdasarkan data forecast untuk mengidentifikasi periode dengan tingkat risiko lingkungan yang relatif lebih rendah.

Aplikasi akan menganalisis kondisi beberapa jam ke depan berdasarkan indikator lingkungan yang tersedia, kemudian menampilkan periode waktu yang memiliki tingkat risiko relatif lebih rendah.

Contoh informasi yang ditampilkan:

> **Waktu dengan risiko lingkungan lebih rendah: 15.00–17.00**

Fitur ini dimaksudkan sebagai informasi pendukung bagi pengemudi dalam mempertimbangkan waktu beraktivitas atau beristirahat, bukan sebagai penentu waktu kerja secara mutlak.

### 8. Deployment & Socialization
Versi aplikasi yang telah dikembangkan akan dideploy dan diperkenalkan kepada kelompok pengemudi ojek online baru, disertai penjelasan mengenai:
- cara membaca kondisi lingkungan
- penggunaan fitur forecast
- penggunaan rekomendasi waktu dengan risiko lingkungan lebih rendah
- penggunaan dark/light mode
- perubahan dan improvement pada versi aplikasi terbaru

### 9. Evaluation
Setelah penggunaan aplikasi, akan dilakukan evaluasi sederhana melalui short post-survey dan dokumentasi hasil untuk mengukur:
- kemudahan penggunaan aplikasi
- kejelasan informasi yang diberikan
- manfaat fitur forecast
- manfaat rekomendasi waktu
- kenyamanan tampilan aplikasi
- feedback terhadap versi aplikasi yang telah dikembangkan

## Expected Outcome

Hasil akhir diharapkan berupa versi **LingkunganSehat** yang lebih stabil, lebih mudah digunakan, dan lebih informatif, dengan peningkatan UI/UX, dukungan dark/light mode, fitur hourly environmental forecast, serta rekomendasi waktu dengan risiko lingkungan yang relatif lebih rendah.
Dua jenis anomali berhasil terdeteksi:
1. Anomali numerik dari `decoy_noise` di atas ambang IQR (Q3 + 1.5×IQR) -> menggunakan konsep quartil untuk mendeteksi outliers/anomaly
2. Kategori `decoy_flag` tertentu (seperti ‘C’/‘D’) memiliki rata-rata `payment_value` jauh di atas kategori lain.
Kombinasi keduanya mendeteksi pola transaksi tidak biasa yang bisa disebabkan oleh data sintetis.
Catatan: Perbedaan hasil deteksi SQL dan Pandas bisa terjadi karena SQLite tidak mendukung fungsi statistik tinggi seperti IQR dan STDDEV, sehingga hasil di SQL lebih kasar.

# Laporan Praktikum 3 – React Query & Caching

**Nama:** Muh Zidan Arif Saputra  
**NIM:** V3424084
**Kelas:** TIC 24
**Mata Kuliah:** Pemrograman Front-End  

---

## Tujuan
Melihat perbedaan waktu respon aplikasi sebelum dan sesudah menggunakan cache, serta memahami cara React Query mengelola data secara otomatis.

---

## Langkah Pengujian
1. Menjalankan aplikasi Point of Sales (POS) sederhana di React.  
2. Mencari produk seperti “produk 5000”.  
3. Melihat hasil di React Profiler dan Console apakah muncul `cache miss` atau `cache hit`.  
4. Mengamati perbedaan waktu render di Profiler.

---

## Hasil
- Saat pencarian pertama kali muncul log “Cache miss”, artinya data belum ada di cache.  
  Render duration sekitar 0.6ms.
- Saat pencarian yang sama dilakukan lagi, muncul log “Cache hit”, berarti data diambil dari cache.  
  Render duration turun jadi 0.4ms.

### Screenshot:
**Cache Miss (pencarian pertama)**  
<img width="1920" height="1054" alt="Screenshot From 2025-11-08 17-33-39" src="https://github.com/user-attachments/assets/bc5d0fd7-fe07-44fc-bcad-434e182ed8bb" />


**Cache Hit (pencarian kedua)**  
<img width="1920" height="1054" alt="Screenshot From 2025-11-08 17-37-11" src="https://github.com/user-attachments/assets/d629a83b-360b-4327-ab88-07e6a475da11" />


---

## Penjelasan
React Query bisa menyimpan hasil pencarian ke dalam cache otomatis, jadi kalau pencarian yang sama dilakukan lagi, data langsung diambil dari cache tanpa perlu menghitung ulang.

---

## Kesimpulan
Menggunakan cache (baik dari localStorage atau React Query) membuat aplikasi jadi **lebih cepat dan efisien**, karena tidak perlu memproses data berulang kali.  
Dengan React Query, pengelolaan cache jadi lebih mudah karena semua diatur otomatis oleh library.

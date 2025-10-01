# DIOS — Dump In One Shot

**DIOS** adalah proof-of-concept (PoC) yang mengekspor hasil query MySQL dalam format HTML terstruktur supaya hasil *database dump* mudah dibaca di browser. Payload ini menggabungkan teknik SQL (mis. concat yang diberi komentar MySQL) dan enkoding hex untuk menghasilkan blok HTML/CSS/JS secara langsung dari hasil query.

> ⚠️ **Penting:** DIOS dibuat semata-mata untuk tujuan **edukasi, riset keamanan, dan pengujian (red team / pentest)** di lingkungan yang Anda miliki atau yang Anda punya izin eksplisit untuk diuji. **Jangan** gunakan alat ini untuk mengeksploitasi sistem tanpa izin.

---

## Fitur utama
- Merender informasi server MySQL (host, versi, user, kompiler OS, port, datadir) ke dalam layout HTML.
- Menampilkan ringkasan hak akses user (privileges) dan metadata `information_schema` (tabel & kolom).
- Mengemas output menggunakan markup HTML yang memakai kelas-kelas Bootstrap untuk tampilan yang rapi.
- Watermark/branding untuk menandai sumber PoC.

---

## Tujuan penggunaan
Alat dan payload di repo ini ditujukan untuk:
- Demonstrasi bagaimana injeksi SQL bisa dimanfaatkan untuk mengambil informasi dari database dan memformatnya untuk tampilan browser.
- Membantu tim keamanan memahami dampak potensi SQL Injection dan bagaimana hasil injeksi dapat terlihat di sisi klien.
- Digunakan pada *lab* pengujian yang terkontrol (mis. VM lokal, container, atau aplikasi intentionally vulnerable seperti DVWA/Mutillidae) untuk latihan mitigasi.

---

## Lingkungan pengujian yang direkomendasikan
Gunakan salah satu opsi berikut untuk melakukan pengujian secara aman:
- Jalankan instance MySQL dan aplikasi web di **mesin lokal** atau **container** (Docker).
- Gunakan aplikasi latihan rentan seperti **Damn Vulnerable Web Application (DVWA)**, **Mutillidae**, atau target CTF yang Anda kontrol.
- Jangan pernah menguji pada sistem produksi atau sistem yang bukan milik Anda tanpa izin tertulis.

---

## Cara pakai (high-level)
1. Pastikan Anda memiliki lingkungan uji (MySQL + aplikasi web rentan) yang berjalan di jaringan yang Anda kontrol.
2. Pelajari file PoC untuk memahami jenis output yang dihasilkan (HTML + table + script).
3. Gunakan payload **hanya** pada parameter dari aplikasi uji yang memang rentan dan hanya untuk demonstrasi.

> Catatan: README ini tidak memuat instruksi eksekusi payload terhadap target nyata. Jika Anda memerlukan panduan implementasi untuk lab internal (mis. cara men-deploy DVWA di Docker dan menguji secara aman), beri tahu saya dan saya bantu dengan instruksi untuk lingkungan yang terkontrol.

---

## Kontribusi
Kami menerima kontribusi yang bersifat pendidikan, perbaikan dokumentasi, dan pengembangan lab pengujian. Jika ingin berkontribusi:
1. Fork repo ini.
2. Buat branch perbaikan.
3. Ajukan pull request dengan deskripsi perubahan.

---

## Etika & Legal
Dengan menggunakan materi di repo ini, Anda menyatakan bahwa penggunaan Anda adalah **legal** dan **etis**. Pemilik repo **tidak bertanggung jawab** atas penyalahgunaan atau konsekuensi hukum akibat penggunaan materi ini pada sistem tanpa izin.

---

## Lisensi
Sertakan lisensi yang sesuai (mis. MIT) atau diskusikan lisensi yang Anda inginkan. Contoh singkat:

```
MIT License
© [tahun] [nama pembuat]
```

---

## Kredit
- PoC & branding awal: DIOS by Raymond7 — ZeroByte.ID
- Template tampilan: Bootstrap (dipakai untuk styling hasil HTML)

---

Jika mau, saya bisa:
- Tambahkan bagian *how-to* untuk men-setup lab (DVWA + MySQL) menggunakan Docker.
- Atau buatkan *CONTRIBUTING.md* dan *CODE_OF_CONDUCT.md* untuk repo.

Mau saya tambahkan salah satunya?


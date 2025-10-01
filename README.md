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

## Etika & Legal
Dengan menggunakan materi di repo ini, Anda menyatakan bahwa penggunaan Anda adalah **legal** dan **etis**. Pemilik repo **tidak bertanggung jawab** atas penyalahgunaan atau konsekuensi hukum akibat penggunaan materi ini pada sistem tanpa izin.

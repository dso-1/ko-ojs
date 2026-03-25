## 1. Mengapa penting mendefinisikan *scope* sebelum melakukan *penetration testing*?

**Jawaban:**
Mendefinisikan *scope* (ruang lingkup) adalah langkah krusial untuk memastikan pengujian tetap terkendali, fokus, dan legal. Alasan utamanya meliputi:

* **Perlindungan Aset Kritis:** Menghindari pengujian pada sistem yang sangat sensitif yang bisa menyebabkan *downtime* atau kerusakan data jika terkena beban pengujian.
* **Aspek Legalitas:** Menentukan batasan hukum agar tim *pentester* tidak secara tidak sengaja menyerang infrastruktur milik pihak ketiga (seperti penyedia *cloud* atau ISP) yang berada di luar wewenang klien.
* **Efisiensi Sumber Daya:** Memastikan tim fokus pada aset yang paling berisiko tinggi (*high-value targets*) sehingga waktu dan biaya yang dikeluarkan lebih optimal.

---

## 2. Apa risiko yang mungkin terjadi jika pengujian dilakukan tanpa *Rules of Engagement* (RoE)?

**Jawaban:**
Melakukan pengujian tanpa RoE formal sangat berbahaya bagi kedua belah pihak (klien dan penguji). Risikonya antara lain:

1.  **Tuntutan Hukum:** Tanpa RoE yang ditandatangani, aktivitas pengujian dapat dianggap sebagai serangan ilegal atau tindak kriminal siber meskipun niatnya baik.
2.  **Gangguan Operasional (Downtime):** Tanpa aturan waktu (kapan pengujian dilakukan) dan metode (apa yang boleh dilakukan), sistem produksi bisa *crash* di jam kerja sibuk dan menghentikan bisnis.
3.  **Respon Insiden Salah Sasaran:** Tim keamanan internal (SOC) mungkin akan merespons pengujian sebagai serangan nyata, membuang sumber daya mereka, atau bahkan melibatkan penegak hukum secara tidak perlu.

---

## 3. Jelaskan perbedaan antara *vulnerability assessment* dan *penetration testing*!

**Jawaban:**
Perbedaan utama terletak pada **kedalaman** dan **tujuan** pengujian. Berikut perbandingannya:

| Fitur | *Vulnerability Assessment* (VA) | *Penetration Testing* (PT) |
| :--- | :--- | :--- |
| **Tujuan Utama** | Mengidentifikasi dan mendata daftar kerentanan yang ada. | Membuktikan apakah kerentanan tersebut dapat dieksploitasi untuk menembus sistem. |
| **Metode** | Dominan menggunakan alat pemindaian otomatis (*automated tools*). | Kombinasi antara alat otomatis dan teknik manual yang kreatif oleh manusia. |
| **Cakupan** | Luas (mencakup banyak aset) namun dangkal. | Fokus pada target spesifik namun sangat mendalam. |
| **Hasil Akhir** | Laporan berisi daftar kerentanan dan skor risikonya. | Bukti nyata akses sistem (*Proof of Concept*) dan dampak serangan. |

---

## 4. Mengapa OJS versi lama masih banyak dipakai di institusi akademik? Apa implikasinya terhadap keamanan?

**Jawaban:**
Banyak institusi akademik masih menggunakan OJS (*Open Journal Systems*) versi lama (seperti versi 2.x) karena beberapa kendala teknis dan manajerial.

### Mengapa Masih Dipakai?
* **Ketergantungan Kustomisasi:** Banyak jurnal telah memodifikasi tampilan atau *plugin* yang tidak kompatibel dengan versi terbaru, sehingga migrasi dianggap berisiko merusak tampilan.
* **Keterbatasan Sumber Daya IT:** Kurangnya staf IT khusus di lingkungan kampus yang memiliki waktu atau keahlian untuk melakukan migrasi data yang kompleks.
* **Kebutuhan Infrastruktur:** Versi terbaru seringkali membutuhkan versi PHP atau database yang lebih modern, yang mungkin belum didukung oleh server lama milik kampus.

### Implikasi Keamanan:
* **Eksploitasi Celah Publik:** Versi lama sering memiliki celah yang sudah diketahui umum (*public exploits*), seperti *Remote Code Execution* (RCE).
* **Penyalahgunaan Reputasi:** Peretas sering menyisipkan konten ilegal (seperti *backlink* judi) ke dalam jurnal, yang mengakibatkan domain `.ac.id` terkena *blacklist* oleh mesin pencari.
* **Kehilangan Integritas Data:** Risiko manipulasi naskah penelitian atau pencurian data akun penulis dan penelaah (*reviewer*).

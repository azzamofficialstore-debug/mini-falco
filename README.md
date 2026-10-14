# Mini Falco

Versi ringan dari **Falco**, AI Social Media Analyst, dibuat oleh Insightory by Nakama Creative Lab.

Mini Falco adalah **bonus pendamping SOP Social Media Analysis Playbook**. Dirancang untuk membantu kamu yang sudah baca playbook supaya bisa langsung praktik, di luar sekedar paham teori.

---

## Apa yang Bisa Mini Falco Lakukan

Mini Falco bantu di tiga hal saja. Tegas, fokus, langsung pakai.

### 1. Outline Analisis (Kerangka Siap Pakai)

Kamu sebut jenis analisis (organik, ads, KOL, liveshopping, kompetitor, atau reporting periodik) + platform + periode, Mini Falco kasih kerangka 6-Step Framework yang sudah kontekstual. Per step ada:

- 3-5 pertanyaan kunci yang harus kamu jawab
- Faktor spesifik yang harus dianalisis
- 2-3 angle insight yang biasanya muncul di jenis analisis itu
- Reminder anti-generik

Outline siap kamu copy paste, isi datanya sendiri.

### 2. Self-Check Deskripsi Konten

Kamu paste deskripsi konten yang kamu tulis (untuk konten organik, ads, KOL, atau live), Mini Falco scan kelengkapan 6 dimensi deskripsi (sesuai Bab 17 playbook) dan flag generik phrase yang ketemu (sesuai Bab 18). Kamu dapat:

- Skor kelengkapan per dimensi: Lengkap, Tipis, atau Kosong
- Flag setiap frasa generik yang ketemu, dengan saran pengganti spesifik
- 2-3 contoh frasa pengganti untuk dimensi yang Tipis atau Kosong

Output siap kamu pakai untuk revisi tulisan kamu sendiri.

### 3. Penjelasan Metric

Kamu sebut satu metric (save rate, ROAS, GMV, CTR, completion rate, ER, AOV, dll) + platform, Mini Falco kasih:

- Definisi platform-specific
- Range sehat sebagai benchmark umum
- 1-2 jebakan baca yang paling sering bikin tersesat
- Metric pasangan yang harus dibaca bareng (contoh: ER tanpa save rate menyesatkan, ROAS tanpa CPA menyesatkan)
- Pointer ke bab playbook untuk dalami

Output ringkas, satu layar, edukatif.

---

## Apa yang Mini Falco TIDAK Lakukan

Penting kamu tahu batasan ini supaya tidak kecewa.

- **Tidak mengerjakan analisis utuh dengan data kamu.** Mini Falco kasih kerangka, di luar isi. Kalau kamu punya 30 konten dan minta dianalisis sampai kesimpulan, itu ranahnya **Falco full**.
- **Tidak menjalankan brand context setup.** Onboarding Mini Falco maksimum 3 pertanyaan teknis (jenis analisis, platform, periode). Kustomisasi spesifik brand butuh setup 12 pertanyaan di Falco full.
- **Tidak menghasilkan kesimpulan dan saran level 3.** Saran level 3 yang punya eksekusi konkret + metrik ukur + target angka + prioritas adalah signature Falco full.
- **Tidak menjalankan Audit 360°.** Mode Audit B dengan 9 blok wajib (profil, executive summary, audit konten, audit ekosistem, analisis eksternal, analisis audiens, gap analysis, rekomendasi, roadmap) ada di Falco full.
- **Tidak iteratif.** Mini Falco one-shot per capability. Setelah outline keluar, sesi capability itu selesai. Untuk deep dive, hypothesis testing, atau comparative analysis, ranahnya Falco full.
- **Tidak menghasilkan file deliverable.** Output di chat saja. Kalau butuh DOCX, PDF, XLSX, ranahnya Falco full.

Untuk kebutuhan di atas, **upgrade ke Falco full**.

---

## Cara Install

### Opsi 1: Claude Pro, Team, atau Enterprise (Direkomendasikan)

1. Buka [claude.ai](https://claude.ai) dan login
2. Klik tombol Upload File di chat box
3. Upload folder `mini-falco/` (zip dulu kalau perlu) atau attach file `SKILL.md` + `SYSTEM-PROMPT.md` + folder `references/` + folder `standards/`
4. Mulai chat dengan: "Halo Mini Falco" atau langsung sebut request kamu (misal: "Bantu outline analisis konten organik IG bulan ini")

Mini Falco akan kenali identitasnya dan langsung kerja sesuai 3 capability.

### Opsi 2: ChatGPT (Custom GPT atau Project)

1. Buat Custom GPT atau Project baru di ChatGPT
2. Upload semua file Mini Falco ke knowledge base GPT
3. Set system instruction ke isi file `SYSTEM-PROMPT.md`
4. Mulai chat seperti biasa

### Opsi 3: AI Lain (Gemini, Perplexity, dll)

Sebagian besar AI yang support file upload bisa pakai Mini Falco. Setup:

1. Upload file Mini Falco
2. Mulai chat dengan: "Mulai sesi sebagai Mini Falco. Baca SKILL.md dan SYSTEM-PROMPT.md sebagai instruction utama."

Catatan: Kualitas output di AI selain Claude bisa berbeda. Untuk hasil paling konsisten, Claude direkomendasikan.

---

## Tips Pakai

### Untuk Capability 1 (Outline)

- **Sebut jenis analisis dengan jelas.** "Analisis konten organik IG" lebih jelas daripada "analisis socmed".
- **Sebut periode.** "Bulan November 2025" lebih jelas daripada "bulan ini".
- **Outline siap kamu adapt.** Bentuknya peta jalan yang masih bisa kamu sesuaikan ke konteks brand, di luar cetak-biru kaku.

### Untuk Capability 2 (Self-Check)

- **Paste deskripsi yang utuh.** Mini Falco scan tulisan kamu apa adanya, di luar yang kamu deskripsikan ulang.
- **Sebut konteks deskripsi.** "Ini deskripsi konten organik" atau "ini deskripsi sesi live".
- **Self-check satu deskripsi per sesi.** Untuk batch deskripsi, lakukan satu per satu.

### Untuk Capability 3 (Metric)

- **Satu metric per sesi.** Kalau tanya banyak metric, output bisa hambar dan terlalu banyak. Pilih satu yang paling kamu butuh dalami.
- **Sebut platform spesifik.** ER di IG ≠ ER di TikTok ≠ ER di LinkedIn. Mini Falco butuh tahu platform untuk kasih jawaban yang tepat.

---

## Upgrade ke Falco Full

Kalau kamu butuh:

- Analisis utuh dengan data brand kamu, dari overview sampai saran level 3
- Brand context setup yang membuat analisis disesuaikan ke positioning, target audience, KPI brand kamu
- Mode Audit 360° dengan 9 blok wajib
- Iterasi konsultatif (deep dive faktor tertentu, hypothesis testing, comparative analysis)
- File deliverable (report DOCX, PDF, dashboard XLSX)
- 8 standar mendalam analisis (mekanisme kenapa, cross-pattern, absence pattern, label keyakinan, hook detail, retention depth, distribusi pareto, saran level 3)

**Akses Falco full di sini:** https://nakama-creative-lab.myscalev.com/falco-ai

Dibuat oleh Insightory by Nakama Creative Lab.

---

## Feedback dan Pertanyaan

Mini Falco adalah produk dalam pengembangan. Kalau ada bug, saran, atau capability tambahan yang kamu rasa harus ada di Mini Falco, kabari vendor playbook (Insightory by Nakama Creative Lab) supaya bisa di-improve di versi berikutnya.

Selamat menganalisis.

# Metric Reading Helper, Reference untuk Capability 3

## Tujuan File Ini

Bahan ringkas untuk Mini Falco menjelaskan **satu metric per sesi** dengan struktur konsisten: definisi, range sehat, 1-2 jebakan baca, metric pasangan. Anchor ke Bab 27 playbook (glossary lengkap) dan Bab 28 (benchmark per kategori).

**Filosofi yang wajib Mini Falco ingatkan ke user:**

1. Setiap platform punya definisi metric berbeda. ER di IG berbeda dengan ER di TikTok dan LinkedIn.
2. Metric tanpa konteks adalah angka mati. Range sehat di file ini cuma baseline, di luar judgment final.

---

## Filosofi Inti, Kunci Socmed Cuma 2

Sebelum baca metric per metric, Mini Falco wajib paham filosofi kunci ini, dan ingatkan ke user kalau relevan:

**Kunci performa socmed cuma 2 hal: ditonton sampai habis (retention) dan interaktif (engagement).**

- **Retention adalah leading indicator.** Konten yang ditonton sampai habis adalah sinyal ke algoritma kalau konten ini layak di-push. Tanpa retention, views gak akan naik.
- **Engagement bagus dan retention bagus akan menghasilkan views bagus.** Dua-duanya kunci, dengan retention sebagai fundamen yang gak bisa di-skip.
- **Tidak ada skenario dimana views bisa bagus saat retention jelek.** Algoritma socmed modern (IG, TikTok, YouTube) prioritisasi retention dulu. Kalau retention jelek, algoritma berhenti push, views stuck.
- **Banyak yang interaksinya bagus tapi retention-nya jelek, views-nya juga jelek.** Kasus klasik: konten yang likes-nya banyak di awal (hook menarik) tapi audience drop di tengah, akhirnya views stuck karena algoritma gak lanjut push.

**Implikasi untuk analisis:** Kalau views jelek, hindari langsung salahin hook atau topik. Cek retention dulu. Kalau retention jelek, fix di sana dulu. Kalau retention bagus dan views masih jelek, baru cek faktor lain (hook 3 detik pertama, topik, timing, dll).

---

## Struktur Output Per Metric (Wajib Konsisten)

```
## [Metric] di [Platform]

**Definisi:** [1-2 kalimat platform-specific]

**Range sehat (benchmark umum):**
- [tier 1: fair]
- [tier 2: strong]
- [tier 3: excellent]

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca yang umum:**
1. [misinterpretation 1]
2. [misinterpretation 2]

**Metric pasangan yang harus dibaca bareng:**
- [metric A]: [alasan singkat]
- [metric B]: [alasan singkat]

[Upselling reminder + redirect ke Bab 27 + Bab 28 + Falco full]
```

---

## Library 16 Metric Paling Umum

Urutan disusun berdasarkan filosofi inti: **Retention Metrics dulu, Engagement Metrics kemudian, Reach Metrics terakhir, Ads/Marketplace Metrics terpisah.** Mini Falco gak harus ngikutin urutan ini saat menjawab, tapi mental model-nya: retention is king.

---

### KATEGORI 1: RETENTION METRICS (Kunci Pertama Socmed)

### 1. Views

**Definisi:** Jumlah kali konten diputar atau ditampilkan. **Definisi berbeda per platform:**
- IG Reels: 1 view dihitung dari 1x putar (autoplay terhitung)
- TikTok: 1 view dihitung dari minimal 1 detik diputar (longgar)
- YouTube: 1 view dihitung dari minimal 30 detik atau 50% durasi (konservatif)

**Range sehat:** Bergantung tier follower dan algoritma boost. Untuk akun mid-size (10K-100K followers), views per konten yang sehat 1-3x dari follower count. Akun yang sering "masuk FYP", multiplier bisa 10-50x.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **Views adalah lagging indicator, di luar leading indicator.** Views tinggi adalah hasil dari retention + engagement yang bagus. Kalau cuma kejar views tanpa fix retention, gak sustainable.
2. **Views lintas platform gak bisa dibandingkan langsung.** 10K views di TikTok berbeda dengan 10K views di YouTube karena definisi view-nya beda.

**Metric pasangan yang harus dibaca bareng:**
- **Retention Rate / AWT:** Views tanpa retention menunjukkan hook-only content (interest awal, gak retain di mid-video). Algoritma gak lanjut push.
- **Reach atau Unique Viewers:** Views tinggi dengan reach kecil menunjukkan konten di-replay banyak (loyal audience), di luar viral.

### 2. Retention Rate / Average Watch Time (AWT)

**Definisi:** Rata-rata durasi user nonton sebelum scroll. Indikator paling penting di TikTok dan IG Reels untuk algoritma push.

**Range sehat:**
- 50-70% dari durasi total: healthy
- 70%+: strong retention
- 90%+ untuk video pendek (sub-15 detik): excellent

**Contoh:** Reels 30 detik dengan AWT 21 detik berarti retention rate 70%. Itu strong.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **AWT tinggi di video pendek (10-15 detik) gak otomatis hook bagus.** Format pendek punya completion bias karena gak ada waktu untuk drop.
2. **AWT bisa di-game dengan loop ending** (video yang ending-nya nyambung ke awal, bikin user nonton ulang tanpa sadar). Cek apakah konten punya loop.

**Metric pasangan yang harus dibaca bareng:**
- **Completion Rate:** AWT 70% bisa berarti retention curve flat (good) atau drop tajam di tengah. Completion rate clarify pattern drop.
- **Hook Retention (3 detik pertama):** AWT total tinggi tapi hook drop tinggi menunjukkan masalah di opening.

### 3. Hook Retention / Skip Rate 3 Detik Pertama

**Definisi:** Persentase user yang LANJUT nonton setelah 3 detik pertama (di luar yang langsung skip). Indikator kekuatan hook.

**Range sehat:**
- 60-70% lanjut nonton (drop 30-40%): fair
- 70-85% lanjut nonton: strong
- 85%+ lanjut nonton: excellent (hook sangat kuat)

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **Hook retention bagus gak otomatis bikin views naik.** Kalau hook kuat tapi mid-video drop, AWT total tetap jelek, algoritma stop push.
2. **Drop di 3 detik pertama paling sering disebabkan thumbnail/cover yang mismatch dengan konten aktual.** User di-tarik masuk tapi langsung skip karena dapet beda dari ekspektasi.

**Metric pasangan yang harus dibaca bareng:**
- **AWT atau Completion Rate:** Hook bagus yang dibarengi AWT bagus menunjukkan full picture retention healthy. Hook bagus yang dibarengi AWT jelek menunjukkan problem di mid-video.
- **Audience Retention Curve (YouTube):** Visualisasi drop point untuk identifikasi kapan user mulai skip.

### 4. Completion Rate

**Definisi:** Persentase user yang nonton video sampai akhir.

**Range sehat:**
- 20-40% untuk video 30-60 detik: fair
- 40-60%: strong
- 60%+: excellent

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **Completion rate sangat bergantung durasi.** Video 10 detik dapat 80% completion adalah default, di luar achievement. Video 60 detik dapat 40% sudah strong.
2. **Completion rate tinggi gak otomatis viral di TikTok.** FYP boost lebih dipengaruhi watch time absolut (jam x viewers), di luar persentase completion.

**Metric pasangan yang harus dibaca bareng:**
- **Average Watch Time:** Completion + AWT kasih full picture retention curve.
- **Replay Rate:** Completion tinggi yang dibarengi replay tinggi menunjukkan konten favorit, sinyal sangat kuat ke algoritma.

---

### KATEGORI 2: ENGAGEMENT METRICS (Kunci Kedua Socmed)

### 5. Engagement Rate (ER), IG dan TikTok

**Definisi:** Persentase audience yang engage (likes + comments + saves + shares) relatif ke reach (IG) atau views (TikTok).

**Range sehat IG (by Reach):** 4-7% fair, 7-10% strong, 10%+ excellent

**Range sehat TikTok (by Views):** 4-7% fair, 7-12% strong, 12%+ excellent

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **ER di IG dan TikTok gak setara,** basis perhitungan berbeda (reach di IG, views di TikTok).
2. **ER tinggi di reach kecil gak otomatis viral,** bisa jadi konten loyal-but-small audience.

**Metric pasangan yang harus dibaca bareng:**
- **Save Rate:** Commitment behavior yang lebih tinggi dari likes.
- **AWT atau Retention:** ER bagus yang dibarengi retention jelek tetap menghasilkan views jelek (algoritma gak push).

### 6. Likes Rate

**Definisi:** Persentase audience yang like konten relatif ke reach (IG) atau views (TikTok). Engagement paling permukaan, paling mudah dilakukan.

**Range sehat:**
- 3-5% fair
- 5-8% strong
- 8%+ excellent

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. **Likes adalah engagement paling lemah.** User bisa like tanpa benar-benar engage (auto-like sambil scroll, like dari thumbnail). Likes rate tinggi gak otomatis konten valuable.
2. **Algoritma modern (TikTok, IG) sudah de-prioritize likes** dibanding save, share, comment quality, dan retention. Likes rate tinggi tapi save rate dan share rate nol menunjukkan konten cuma "lewat".

**Metric pasangan yang harus dibaca bareng:**
- **Save Rate dan Share Rate:** Likes rate tinggi + save/share rate nol menunjukkan engagement permukaan. Likes rate tinggi + save/share rate bagus menunjukkan engagement berlapis.
- **Comments quality:** Komentar berisi pertanyaan atau diskusi menunjukkan engagement yang lebih dalam dari likes.

### 7. Save Rate, IG

**Definisi:** Persentase audience yang save konten relatif ke reach. Commitment behavior, di luar engagement permukaan.

**Range sehat:** 1-2% fair, 2-4% strong (konten reference atau utility), 4%+ excellent (sangat valuable).

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. Save rate tinggi di konten viral satu kali gak sustainable, cek konsistensi di multiple konten.
2. Save bisa pasif (auto-save tanpa intent revisit), cek apakah konten yang save rate tinggi juga punya share rate tidak nol.

**Metric pasangan yang harus dibaca bareng:**
- **Share Rate:** Social currency indicator.
- **Comments quality:** Authority indicator.

### 8. Share Rate, IG dan TikTok

**Definisi:** Persentase audience yang share konten relatif ke reach atau views.

**Range sehat:** 0.3-1% fair, 1-3% strong, 3%+ excellent (potensi viral).

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. Share rate tinggi di konten kontroversial gak otomatis brand-positive, share bisa dari angry-engagement.
2. Share di Story (re-share) lebih impactful daripada Send to friend. IG Insight kadang campur kedua jenis.

**Metric pasangan yang harus dibaca bareng:**
- **Save Rate:** Save dan Share dibaca bareng menunjukkan social currency + personal utility.
- **Comments quality:** Komentar emosional sering driver share.

---

### KATEGORI 3: ADS METRICS

### 9. Click-Through Rate (CTR), Ads dan YouTube

**Definisi:** Persentase impressions yang menghasilkan klik.

**Range sehat Ads:** 0.5-1% fair (awareness), 1-2% strong (traffic), 2%+ excellent (atau retargeting).

**Range sehat YouTube:** 2-5% fair, 5-10% strong, 10%+ excellent.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. CTR tinggi gak otomatis convert. Click ke landing page berbeda dengan purchase.
2. CTR di-influence sangat oleh creative dan placement. Bandingkan apple-to-apple (CTR Reels vs CTR Feed, di luar CTR overall).

**Metric pasangan yang harus dibaca bareng:**
- **CPC:** Efisiensi click.
- **Conversion Rate:** Efektivitas end-to-end.

### 10. CPM (Cost per Mille), Ads

**Definisi:** Cost per 1000 impressions.

**Range sehat Indonesia:** Rp 20-50K untuk Feed IG, Rp 10-30K untuk Reels, lebih tinggi untuk LinkedIn, lebih rendah untuk Audience Network.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. CPM rendah gak otomatis efisien. CPM rendah di Audience Network sering disertai CTR sangat rendah dan kualitas traffic buruk.
2. CPM naik di periode kompetitif (Lebaran, akhir tahun, awal bulan) adalah dynamic pasar, di luar masalah ads kamu.

**Metric pasangan yang harus dibaca bareng:**
- **CTR:** Efektivitas reach + click.
- **CPC:** CPM rendah dengan CPC tinggi menunjukkan traffic banyak yang tidak klik.

### 11. CPC (Cost per Click), Ads

**Definisi:** Cost per klik. Formula: Spend / Clicks.

**Range sehat Indonesia:** Rp 500-2000 cold broad, Rp 200-500 retargeting, Rp 2000-5000 niche kompetitif.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. CPC rendah gak otomatis bagus kalau click-nya tidak convert. Cek CPA.
2. CPC bisa di-game dengan creative bait. Cek bounce rate di landing page.

**Metric pasangan yang harus dibaca bareng:**
- **CPA:** Efisiensi conversion.
- **Conversion Rate:** Match traffic dengan offering.

### 12. CPA (Cost per Acquisition), Ads

**Definisi:** Cost per conversion (purchase, signup, dll).

**Range sehat:** Sangat bergantung price point. Produk Rp 100K, CPA sehat Rp 20-50K. Produk Rp 1jt, CPA sehat Rp 100-300K.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. CPA rendah di traffic kecil (10 conversions) gak statistical significant. Tunggu 50+ conversions baru evaluate.
2. CPA naik di periode launching produk baru adalah ekspektasi. Tunggu learning phase keluar.

**Metric pasangan yang harus dibaca bareng:**
- **ROAS:** Full picture efficiency.
- **Conversion Rate:** Identifikasi sumber masalah.

### 13. ROAS (Return on Ad Spend), Ads

**Definisi:** Revenue dari ads dibagi spend ads.

**Range sehat:** 1-2x break-even, 2-4x healthy, 4x+ strong dan sangat profitable.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. ROAS attribution di platform sering over-claim. Cek dengan metode incrementality test untuk ground truth.
2. ROAS tinggi di retargeting gak setara ROAS tinggi di cold acquisition. Pisahkan funnel.

**Metric pasangan yang harus dibaca bareng:**
- **CPA:** Efisiensi per acquisition.
- **AOV:** Driver ROAS, naik karena bundle atau karena CR naik.

---

### KATEGORI 4: MARKETPLACE & LIVE METRICS

### 14. Conversion Rate (CR), Marketplace dan Landing Page

**Definisi:** Persentase visitor yang melakukan transaksi atau conversion action.

**Range sehat Marketplace:** 1-3% fair (produk umum), 3-5% strong, 5%+ excellent (atau produk niche high-intent).

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. CR tinggi di traffic kecil (50 visitors) gak statistical significant. Cek minimal 500-1000 visitors.
2. CR drop di periode promo gak otomatis bad, bisa karena traffic naik dari curious shoppers (di luar buyers).

**Metric pasangan yang harus dibaca bareng:**
- **AOV:** CR tinggi dengan AOV rendah menunjukkan volume tinggi margin tipis.
- **Repeat Buyer Rate:** Sustainability indicator.

### 15. AOV (Average Order Value), Marketplace

**Definisi:** Rata-rata nilai per transaksi.

**Range sehat:** Bergantung kategori. Skincare premium 200-500K, FMCG 50-150K, fashion 100-300K. Cek benchmark per kategori di Bab 28.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. AOV naik gak otomatis bagus kalau drive-nya bundling murah (volume orders turun). Cek total orders dan total GMV bareng.
2. AOV drop di flash deal adalah ekspektasi, gak alarming kalau total GMV naik.

**Metric pasangan yang harus dibaca bareng:**
- **Total Orders:** AOV dikali Orders menghasilkan GMV.
- **Repeat Buyer AOV:** Biasanya 1.5-2x first-time.

### 16. Peak Viewers, Liveshopping

**Definisi:** Jumlah maksimum concurrent viewers di satu titik selama live.

**Range sehat:** Bergantung tier akun dan promo strategy. Spike biasanya di 30 menit pertama (kalau hero product di awal) atau di flash deal moments.

⚠️ Range di atas benchmark umum. Range spesifik untuk brand kamu bergantung kategori dan tier follower. Untuk benchmark per kategori, baca Bab 28 playbook.

**Jebakan baca:**
1. Peak tinggi sebentar gak setara konsisten viewers tinggi. Cek average concurrent viewers, di luar peak.
2. Peak dari ads pre-live di-boost artifisial. Pisahkan source viewers (organic, ads, notification).

**Metric pasangan yang harus dibaca bareng:**
- **Total Viewers:** Breadth + reach.
- **AWT:** Peak tinggi dengan AWT pendek menunjukkan curi-and-bounce.
- **Conversion Rate:** Engaged vs convert.

---

## Yang Tidak Mini Falco Cakup di File Ini

Metric yang TIDAK ada di library di atas, Mini Falco redirect ke Bab 27 playbook:

- Reach, Impressions, Profile Visits, Follow dari Konten (IG metrics tier 2)
- Traffic Source FYP, Reached Audience (TikTok detail metrics)
- Watch Time Total, Audience Retention Curve, CTR Thumbnail YouTube (YouTube detail)
- Visitors, GMV, Search Keyword (Marketplace tier 2)
- ERR Liveshopping, Total Viewers, ATC Rate (Live detail)
- Frequency, Funnel Position, Landing Page metrics (Ads detail)

Kalau user tanya metric yang tidak ada di library, Mini Falco bilang: "Untuk metric ini, Mini Falco belum punya entry detail. Untuk definisi platform-specific + range sehat + jebakan baca yang lengkap, baca **Bab 27 playbook**. Kalau metric ini critical buat analisis kamu sekarang, kerjanya Falco full karena Falco full akses langsung ke benchmark dan kontekstualisasi ke brand kamu."

---

## Cara Mini Falco Menerapkan Metric Helper

1. **Identifikasi metric** dari paste-an user. Kalau tidak jelas, tanya.
2. **Identifikasi platform.** ER di IG berbeda dengan ER di TikTok.
3. **Cek apakah metric ada di library** 16 metric di atas. Kalau tidak, redirect ke Bab 27.
4. **Kalau user tanya tentang views jelek atau performa rendah,** Mini Falco prompted untuk tanya balik: "Sudah cek retention rate dan AWT? Karena kunci socmed cuma 2: retention dan engagement. Kalau retention jelek, views juga akan jelek."
5. **Susun output** dengan struktur konsisten: definisi, range sehat dengan disclaimer, 1-2 jebakan baca, metric pasangan, pointer playbook.
6. **Disclaimer benchmark wajib eksplisit.**
7. **Tutup dengan upselling reminder + redirect pattern.**

---

## Catatan Penting untuk Mini Falco

1. **Output ringkas, 1 layar.** Pilih 1-2 jebakan baca yang paling sering bikin tersesat, di luar daftar semuanya.
2. **Satu metric per sesi.** Kalau user tanya 3 metric sekaligus, jawab satu (yang paling top-of-mind) dan ajak user pilih untuk dalami.
3. **Jangan terapkan ke data spesifik user.** Mini Falco tidak baca angka brand user. Kontekstualisasi adalah kerjaan Falco full.
4. **Tegaskan filosofi inti kalau relevan:** retention adalah leading indicator, views adalah lagging indicator.
5. **Multi-pass humanize scan** sebelum kirim.

---

## Closing Block (Wajib di Akhir Setiap Output Capability 3)

Setelah penjelasan metric, Mini Falco tutup dengan closing block dengan flow 2-tahap.

### Tahap 1, Setelah Output Capability (Sekaligus, 1 Message)

```
📚 Untuk dalami lebih lanjut:
- Daftar metric lengkap di semua platform: **Bab 27 playbook**
- Benchmark per kategori brand: **Bab 28 playbook**

🚀 Btw, paham metric itu satu hal. Aplikasi ke angka brand kamu spesifik, kontekstualisasi ke benchmark internal, dan narik kesimpulan strategis itu hal lain. Untuk yang kayak gini, biasanya kakak Mini Falco (Falco full) yang handle. Dia bisa ambil metric brand kamu, frame ke benchmark internal (di luar industri generic), dan kasih diagnosis "kenapa angkanya gini" dengan mekanisme yang jelas.

Detail Falco full di sini: https://nakama-creative-lab.myscalev.com/falco-ai

💬 Btw, kalau boleh tahu, kenapa nih lagi mau dalami metric ini? Lagi ada angka yang kelihatan aneh di brand kamu, atau lagi mau bangun framework KPI sendiri?
```

### Tahap 2, Setelah User Jawab Pain Point

Mini Falco buka file `references/upsell-bridging.md`, cari pain point paling mirip, bridging personalized:

```
[Acknowledgment, restate pain user]
"Oh, jadi kamu lagi ngeliat [restate situasi user]. Make sense banget kenapa kamu cari pemahaman metric ini dulu."

[Bridging ke capability Falco full + benefit + outcome]
"Untuk yang kayak gini, kakak Mini Falco (Falco full) yang lebih cocok. Karena dia [capability spesifik], benefit-nya buat kamu: [outcome konkret yang nyambung]."

[Reinforce link]
"Detail Falco full: https://nakama-creative-lab.myscalev.com/falco-ai"

[Optional, tawarin lanjut di Mini Falco]
"Atau kalau kamu mau dalami metric lain dulu di Mini Falco, tinggal bilang aja."
```

**Catatan:** Filosofi inti "retention adalah leading indicator" tetap muncul kalau relevan dengan pain user. Misal user bilang "konten saya engagement bagus tapi views jelek", ini langsung pas dengan filosofi inti, dan Mini Falco bisa kaitkan ke Falco full yang bisa diagnosis akar masalahnya dengan 8 standar mendalam.

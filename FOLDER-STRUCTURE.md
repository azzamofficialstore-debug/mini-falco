# Mini Falco, Folder Structure dan Perbandingan dengan Falco Induk

## Visual Tree

```
mini-falco/
├── README.md                              # Untuk pembeli playbook, cara install, tips pakai
├── SKILL.md                               # Definisi 3 capability + guardrails redirect
├── SYSTEM-PROMPT.md                       # Persona, prinsip berpikir, anti-pattern
├── FOLDER-STRUCTURE.md                    # File ini, peta folder dan perbandingan
│
├── standards/
│   └── humanize-writing-guide.md          # Protokol humanize zero tolerance
│                                          # Di-copy dari Falco induk untuk konsistensi
│
└── references/
    ├── outline-builder.md                 # Bahan untuk Capability 1 (Outline Generator)
    │                                      # 6 template per jenis analisis
    │
    ├── description-check.md               # Bahan untuk Capability 2 (Self-Check)
    │                                      # 6 dimensi per konteks + 8 kategori generik phrase
    │
    ├── metric-helper.md                   # Bahan untuk Capability 3 (Metric Helper)
    │                                      # Library 16 metric per platform + filosofi retention
    │
    └── upsell-bridging.md                 # Mapping pain point user ke capability Falco full
                                           # Untuk Tahap 2 upsell flow (personalized bridging)
```

**Total:** 9 file di 3 level folder.

---

## Perbandingan dengan Falco Induk

### Falco Induk (Falco Full)

```
falco-skill/
├── SKILL.md
├── SYSTEM-PROMPT.md
├── FOLDER-STRUCTURE.md
├── README.md
│
├── frameworks/
│   ├── six-step-analysis.md
│   ├── faktor-analisis-checklist.md
│   ├── audit-360-framework.md
│   └── ... (file framework lain)
│
├── standards/
│   ├── standar-humanize-writing.md
│   ├── standar-deskripsi-data.md
│   ├── anti-generik-rules.md
│   ├── standar-analisis-mendalam.md
│   ├── standar-saran-level-3.md
│   └── ... (file standar lain)
│
└── references/
    ├── glossary-metrics.md
    ├── benchmark-per-kategori.md
    ├── brand-context-template.md
    ├── brief-collection-templates.md
    └── ... (file referensi lain)
```

Falco induk punya 14+ file di 3 level folder, mencakup framework analisis, standar mendalam, template brand context, glossary, benchmark, dll.

### Mini Falco

```
mini-falco/
├── README.md
├── SKILL.md
├── SYSTEM-PROMPT.md
├── FOLDER-STRUCTURE.md
├── standards/
│   └── humanize-writing-guide.md
└── references/
    ├── outline-builder.md
    ├── description-check.md
    └── metric-helper.md
```

Mini Falco punya 8 file di 3 level folder.

---

## Daftar File: Same, Derived, Exclusive, Excluded

### Sama Persis (Copy Verbatim dari Falco Induk)

| File Mini Falco | Sumber di Falco Induk | Alasan |
|---|---|---|
| `standards/humanize-writing-guide.md` | `standards/standar-humanize-writing.md` | Protokol humanize zero tolerance harus konsisten antara Mini dan Full. Aturan ini override semua. |

### Derived (Diturunkan dari Falco Induk, Disederhanakan)

| File Mini Falco | Sumber di Falco Induk | Yang Berubah |
|---|---|---|
| `SKILL.md` | `SKILL.md` Falco induk + struktur capability baru | Mini Falco hanya 3 capability (di luar 6 capability + 2 mode Falco induk). Onboarding 1-3 pertanyaan (di luar 12 pertanyaan brand setup). Hard limit ditegaskan. |
| `SYSTEM-PROMPT.md` | `SYSTEM-PROMPT.md` Falco induk | Inherit identitas, tone, dan prinsip berpikir Falco. Tambah 6 anti-pattern khusus untuk Mini. Tegaskan posisi sebagai bonus playbook. |
| `references/outline-builder.md` | `frameworks/six-step-analysis.md` + `frameworks/faktor-analisis-checklist.md` + Bab 10-15 playbook | Distill 6-Step Framework jadi outline kosong + 6 template kontekstual per jenis analisis. Tidak ada eksekusi analisis. |
| `references/description-check.md` | `standards/standar-deskripsi-data.md` (Bab 17 playbook) + `standards/anti-generik-rules.md` (Bab 18) | Distill 6 dimensi deskripsi + 8 kategori generik phrase ke format self-check. Tidak ada rewrite total deskripsinya. |
| `references/metric-helper.md` | Bab 27 playbook (Glossary Metrics per Platform) | Distill metric library jadi format edukasi: definisi + range sehat + jebakan baca + metric pasangan. Tidak ada kontekstualisasi ke data spesifik brand. |

### Exclusive (File Khusus Mini Falco, Tidak Ada di Falco Induk)

| File Mini Falco | Alasan Exclusive |
|---|---|
| `README.md` versi Mini | Ditujukan untuk pembeli playbook, di luar developer atau analyst yang pakai Falco full. Posisi sebagai bonus pendamping playbook ditegaskan. |
| `FOLDER-STRUCTURE.md` versi Mini | File ini sendiri. Berfokus pada perbandingan dengan Falco induk dan menjelaskan apa yang dipotong. |

### Excluded (File Falco Induk yang TIDAK Diturunkan ke Mini)

Daftar file Falco induk yang **sengaja tidak diturunkan** ke Mini Falco supaya pembeda tegas:

| File yang Tidak Diturunkan | Alasan |
|---|---|
| `frameworks/audit-360-framework.md` | Mode B Audit 360° dengan 9 blok wajib adalah signature Falco full. Mini Falco tidak punya mode audit. |
| `standards/standar-analisis-mendalam.md` | 8 standar mendalam (mekanisme, cross-pattern, absence, label keyakinan, hook detail, retention depth, distribusi pareto, saran level 3) adalah depth signature Falco full. Mini Falco hanya pakai standar dasar. |
| `standards/standar-saran-level-3.md` | Saran level 3 (eksekusi + metrik ukur + target + prioritas) adalah output signature Falco full. Mini Falco tidak menghasilkan saran. |
| `references/brand-context-template.md` | Brand setup 12 pertanyaan adalah onboarding signature Falco full. Mini Falco maksimum 3 pertanyaan onboarding. |
| `references/brief-collection-templates.md` | 7 pertanyaan brief per analisis adalah Falco full. Mini Falco tidak collect brief. |
| `references/benchmark-per-kategori.md` | Benchmark per kategori brand adalah Bab 28 playbook. Mini Falco hanya kasih disclaimer dan pointer ke Bab 28, tidak include benchmark detail di reference file sendiri. |

---

## Filosofi Struktur Mini Falco

### Kenapa Hanya 8 File?

Setiap file Mini Falco punya alasan ada:

1. **README.md:** Pembeli playbook butuh quick guide cara install dan apa yang Mini Falco bisa
2. **SKILL.md:** AI yang load Mini Falco butuh definisi capability + guardrails
3. **SYSTEM-PROMPT.md:** AI butuh persona, prinsip, anti-pattern
4. **FOLDER-STRUCTURE.md:** Developer atau curious user butuh peta dan konteks
5. **standards/humanize-writing-guide.md:** Protokol humanize harus selalu accessible
6. **references/outline-builder.md:** Bahan untuk capability 1
7. **references/description-check.md:** Bahan untuk capability 2
8. **references/metric-helper.md:** Bahan untuk capability 3

Lebih sedikit dari ini, kualitas output drop. Lebih banyak dari ini, scope creep mulai (Mini Falco mulai mirip Falco full).

### Kenapa standards/ Cuma 1 File?

Falco induk punya banyak file di `standards/` (humanize, deskripsi data, anti-generik, analisis mendalam, saran level 3, dll). Mini Falco hanya pakai humanize karena:

- **Anti-generik dan deskripsi data** sudah di-distill ke `references/description-check.md` (digabung biar focused per capability, versi ringkas)
- **Analisis mendalam dan saran level 3** dipotong total karena out of scope Mini Falco
- **Humanize** harus tetap stand-alone karena ini protokol yang berlaku di setiap output, di atas reference per capability

### Kenapa references/ Cuma 3 File?

Karena Mini Falco hanya punya 3 capability, dan setiap capability punya satu reference file. Mapping 1-to-1 ini bikin AI Mini Falco mudah cari bahan saat eksekusi capability.

### Filosofi Ringkas Per File Reference

Tiap file reference di Mini Falco sengaja dibatasi ukurannya supaya tidak duplikasi konten Falco full:

- **outline-builder.md (~250 baris):** 6 template, masing-masing cuma heading 6-step + 3-5 pertanyaan kunci. Skip detail faktor analisis, angle insight, dan reminder anti-generik per step (itu kedalaman Falco full)
- **description-check.md (~120 baris):** Checklist 6 dimensi per konteks dalam format tabel ringkas + quick reference 8 kategori generik phrase. Skip eksplorasi mendalam tiap kategori (itu Bab 18 playbook)
- **metric-helper.md (~230 baris):** 12 metric paling umum × struktur konsisten (definisi, range, jebakan, pasangan). Skip metric tier 2 dan tier 3 (redirect ke Bab 27)

---

## Comparison Quick-Reference Table

| Aspek | Mini Falco | Falco Full |
|---|---|---|
| Total file | 8 | 14+ |
| Folder | 3 (root, standards/, references/) | 4 (root, frameworks/, standards/, references/) |
| Capability | 3 (Outline, Self-Check, Metric Helper) | 6 (Organik, Ads, KOL, Live, Kompetitor, Reporting) + 2 mode (Analytics A, Audit B) |
| Onboarding | 1-3 pertanyaan teknis | 12 pertanyaan Brand Setup + 7 pertanyaan brief |
| Output format | Chat dengan markdown | Chat + file deliverable (DOCX, PDF, XLSX) |
| Iterasi | One-shot | Konsultatif, multi-turn, deep dive |
| Standar mendalam | Tidak ada | 8 standar wajib |
| Audit Mode | Tidak ada | Mode B dengan 9 blok wajib |
| Posisi | Bonus pendamping playbook | Produk berbayar terpisah |

---

## Catatan untuk Developer atau Vendor Playbook

Mini Falco didesain untuk **bundling FREE** dengan SOP Social Media Analysis Playbook. Strategi:

1. **Pembeli playbook download Mini Falco** sebagai bonus pendamping
2. **Mini Falco bantu pembeli langsung praktik** capability 1-3, sehingga playbook tidak hanya teori
3. **Setiap output Mini Falco anchor ke bab playbook** (Bab 7, 14, 17, 18, 27, 28), supaya pembaca yang mau dalami langsung ke sumbernya
4. **Setiap output Mini Falco redirect ke Falco full** untuk capability di luar scope, supaya yang butuh kedalaman bisa upgrade

Hubungan tiga-arah (Mini Falco - Playbook - Falco full) jadi ekosistem produk yang konsisten.

Untuk versi Falco full, hubungi Insightory by Nakama Creative Lab.

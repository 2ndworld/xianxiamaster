---
name: xianxia-context-compiler
description: "Gunakan ketika akan merencanakan atau menulis bab dan perlu menyusun konteks minimum dari preferensi, reader canon, secret canon, serta state terbaru tanpa membocorkan spoiler."
version: "0.2.0"
---

# xianxia-context-compiler

## Tujuan

Menghasilkan paket konteks kecil, relevan, dan dapat diaudit. Skill ini mencegah dua kegagalan: terlalu sedikit konteks sehingga canon rusak, dan terlalu banyak konteks sehingga model bingung atau membocorkan rahasia.

## Gunakan ketika

Gunakan ketika akan merencanakan atau menulis bab dan perlu menyusun konteks minimum dari preferensi, reader canon, secret canon, serta state terbaru tanpa membocorkan spoiler.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- chapter target;
- POV character;
- reader canon;
- secret canon;
- hard preferences;
- soft/adaptive preferences;
- recent chapter summaries;
- active arc state;
- power-system rules;
- terminology policy dan canonical glossary.

## Output wajib

JSON sesuai `chapter-context.schema.json`, termasuk:
- `reader_known`;
- `secret_constraints`;
- `active_threads`;
- `character_state`;
- `progression_limits`;
- `style_profile`;
- `terminology_policy`;
- canonical terms relevan;
- `forbidden_reveals`;
- `retrieval_trace`.

## Workflow

1. Tentukan tujuan bab dan POV.
2. Ambil fakta yang langsung memengaruhi keputusan atau persepsi POV.
3. Ambil thread aktif yang perlu dibayar, diperdalam, atau dijaga.
4. Masukkan rahasia hanya sebagai constraint internal, bukan kalimat yang siap muncul.
5. Daftarkan reveal yang dilarang.
6. Singkirkan lore yang tidak memiliki fungsi pada bab.
7. Cantumkan sumber setiap fakta pada `retrieval_trace`.
8. Validasi bahwa semua entitas yang dirujuk memiliki ID canon.

## Aturan keras

- Tidak boleh mengubah canon.
- Tidak boleh membuat twist atau fakta baru.
- Tidak boleh memasukkan jawaban misteri ke `reader_known`.
- Rahasia harus ditulis sebagai batas keputusan, bukan prosa pembaca.
- Context budget harus diprioritaskan: hard rule → current state → active thread → style → lore.

## Checklist selesai

- [ ] Tidak ada secret term di reader-known.
- [ ] Semua fakta memiliki sumber.
- [ ] Hanya karakter/lokasi relevan yang masuk.
- [ ] Progression limit tersedia.
- [ ] Batas POV jelas.
- [ ] Konteks cukup untuk menulis bab tanpa membaca keseluruhan novel.

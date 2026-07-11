---
name: xianxiamaster
description: "Gunakan untuk merencanakan, menulis, mengaudit, merevisi, dan meng-commit bab novel xianxia personal dengan narasi Indonesia, istilah dunia Inggris, canon jangka panjang, dan perlindungan spoiler."
version: "0.2.0"
---

# XianxiaMaster

## Tujuan

Menjadi skill orkestrator utama untuk menghasilkan novel xianxia serial yang enak dibaca, konsisten, personal, dan tetap mengejutkan pembaca. Skill ini memanggil sub-skill secara bertahap; ia bukan mega-prompt yang mengerjakan semua tahap sekaligus.

## Kebijakan bahasa

Gunakan standar:

> **Indonesian prose, English world terminology.**

Narasi, dialog, emosi, tindakan, dan penjelasan umum menggunakan bahasa Indonesia. Seluruh nama resmi dunia menggunakan bahasa Inggris kanonik, termasuk realm, stage, technique, pill, herb, artifact, city, sect, clan, kingdom, formation, monster, trial, dan secret realm.

Contoh benar:

- `Early Foundation Realm`
- `Blood Meridian Pill`
- `Blackstone City`
- `Silent River Sect`
- `Soul-Binding Coffin`

Contoh salah:

- `Ranah Foundation Awal`
- `Pil Meridian Darah`
- `Kota Batu Hitam`
- `Sekte Sungai Sunyi`

## Mode default

Mode default adalah **Reader Mode**:

- AI menjadi penulis utama.
- Pembaca tidak perlu mengarahkan plot setelah setiap bab.
- Rencana kitab, twist, motif tersembunyi, dan secret canon tidak ditampilkan.
- Feedback pengguna memengaruhi kecenderungan cerita, bukan menentukan kejadian berikutnya.

## Pipeline wajib

1. `xianxia-context-compiler`
2. `xianxia-arc-planner` bila replanning diperlukan
3. `xianxia-chapter-brief`
4. `xianxia-prose-drafter`
5. `xianxia-dialogue-voice`
6. `xianxia-terminology-guard`
7. `xianxia-progression-guard`
8. `xianxia-continuity-auditor`
9. `xianxia-reader-sim`
10. `xianxia-final-reviser` bila perlu
11. audit ulang
12. `xianxia-state-committer`

## Hard gates

Bab tidak boleh diterbitkan atau di-commit bila masih terdapat:

- spoiler leak;
- pelanggaran aturan keras pengguna;
- terjemahan atau variasi istilah kanonik;
- kontradiksi canon;
- knowledge leak antar-karakter;
- lompatan realm tanpa dasar;
- artefak atau teknik tanpa setup;
- kesalahan timeline material;
- canon delta yang ambigu.

## Aturan orkestrasi

- Muat hanya konteks yang diperlukan untuk satu tahap.
- Jangan memberikan seluruh secret canon kepada reader simulator.
- Draft bukan canon.
- Outline bukan canon.
- Canon hanya berubah setelah bab final lolos seluruh hard gate.
- Gunakan pemeriksaan deterministik untuk aturan objektif dan penilaian LLM untuk kualitas kreatif.
- Maksimal dua revisi otomatis untuk MVP sebelum memakai fallback model atau menandai retry.

## Input minimum

- hard dan soft preferences;
- reader canon;
- secret canon;
- state bab terakhir;
- rencana kitab rahasia;
- terminology policy;
- canonical glossary;
- power-system rules;
- target panjang bab.

## Output

- bab final untuk pembaca;
- laporan audit internal;
- reader-facing summary bebas spoiler bila dibutuhkan;
- canon delta terstruktur;
- metadata versi model, prompt, dan skill.

## Checklist selesai

- [ ] Narasi Indonesia dan istilah dunia Inggris.
- [ ] Tidak ada spoiler internal.
- [ ] POV dan knowledge boundary konsisten.
- [ ] Realm, technique, pill, artifact, dan inventory valid.
- [ ] Bab memiliki perubahan state yang bermakna.
- [ ] Ending pull organik, bukan cliffhanger palsu.
- [ ] Seluruh hard gate lulus.
- [ ] Canon delta dapat di-rollback.

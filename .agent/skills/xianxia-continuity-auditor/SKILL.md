---
name: xianxia-continuity-auditor
description: "Gunakan setelah draft untuk mendeteksi kontradiksi karakterisasi, fakta, timeline, worldbuilding, POV knowledge, dan kebocoran secret canon."
version: "0.2.0"
---

# xianxia-continuity-auditor

## Tujuan

Memberikan audit berprioritas yang dapat ditindaklanjuti. Auditor tidak memperindah prosa dan tidak mengubah plot tanpa instruksi revisi.

## Gunakan ketika

Gunakan setelah draft untuk mendeteksi kontradiksi karakterisasi, fakta, timeline, worldbuilding, POV knowledge, dan kebocoran secret canon.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- draft;
- compiled context;
- committed canon;
- reader canon;
- secret canon;
- previous chapter end state;
- hard preferences.

## Output wajib

JSON sesuai `chapter-audit.schema.json`:
- hard_failures;
- soft_issues;
- evidence spans;
- canon references;
- repair suggestions;
- spoiler_leak status;
- pass/fail.

## Workflow

1. Audit spoiler leak lebih dahulu.
2. Audit hard preference.
3. Audit karakterisasi dan knowledge boundary.
4. Audit fakta, lokasi, inventory, luka, dan hubungan.
5. Audit timeline dan urutan sebab-akibat.
6. Audit aturan dunia.
7. Audit setup/payoff.
8. Audit consistency terminology policy dan glossary.
9. Beri severity dan bukti teks.
10. Sarankan perubahan terkecil yang menyelesaikan akar masalah.

## Aturan keras

- Jangan menganggap beda kata sebagai kontradiksi jika makna konsisten.
- Jangan menandai unreliable narration sebagai error tanpa bukti.
- Jangan memperlihatkan isi secret canon dalam laporan yang dapat dilihat pengguna.
- Diagnosis harus menyebut evidence dan canon source.
- Hard failure bernilai nol sebelum commit.

## Checklist selesai

- [ ] Semua issue memiliki severity.
- [ ] Semua hard issue memiliki evidence.
- [ ] Secret detail disamarkan pada public report.
- [ ] Character knowledge diperiksa.
- [ ] Timeline diperiksa.
- [ ] Hasil akhir pass/fail tegas.

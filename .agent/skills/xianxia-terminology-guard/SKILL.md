---
name: xianxia-terminology-guard
description: "Gunakan setelah drafting dan sebelum continuity audit untuk memastikan seluruh nama dunia memakai bahasa Inggris kanonik, sementara narasi dan dialog tetap bahasa Indonesia."
version: "0.2.0"
---

# xianxia-terminology-guard

## Tujuan

Menjalankan kebijakan **Indonesian prose, English world terminology** secara konsisten pada seluruh novel.

## Gunakan ketika

Gunakan setelah draft atau revisi menghasilkan teks yang mengandung realm, stage, technique, pill, herb, artifact, city, sect, clan, kingdom, faction, monster, formation, trial, atau istilah dunia lainnya.

## Jangan gunakan ketika

- teks bukan bagian novel;
- glossary canon belum tersedia;
- tugas hanya memeriksa struktur plot;
- nama yang diperiksa masih placeholder internal.

## Input wajib

- draft bab;
- terminology policy;
- canonical glossary;
- daftar alias resmi;
- daftar istilah baru yang diusulkan;
- reader canon dan secret canon relevan.

## Output wajib

- canonical terms found;
- forbidden variants found;
- untranslated named terms;
- accidental Indonesian translations;
- capitalization mismatches;
- category mismatches;
- proposed new terms;
- corrected patch list;
- pass/fail.

## Workflow

1. Ekstrak semua kandidat nama dunia.
2. Cocokkan secara case-sensitive dengan glossary.
3. Deteksi terjemahan Indonesia dari istilah kanonik.
4. Deteksi variasi format realm.
5. Periksa suffix kategori seperti `Sect`, `Clan`, `City`, `Kingdom`, `Pill`, dan `Formation`.
6. Bedakan nama resmi dari kata generik dalam narasi.
7. Pertahankan narasi dan dialog dalam bahasa Indonesia.
8. Untuk istilah baru, buat proposal nama bahasa Inggris dan category ID.
9. Jangan memasukkan istilah baru ke canon sebelum state committer.
10. Berikan patch terkecil.

## Aturan keras

- Jangan menerjemahkan nama kanonik.
- Jangan memakai bilingual alias kecuali `use_bilingual_aliases=true`.
- Jangan mengubah `Silent River Sect` menjadi `Silent River Clan`.
- Jangan mengubah kapitalisasi atau tanda hubung nama kanonik.
- Jangan membuat format campuran seperti `Ranah Foundation Awal`.
- Jangan mengubah kata generik Indonesia menjadi bahasa Inggris secara berlebihan.
- Jangan mengganti nama karakter hanya karena terdengar non-Inggris.

## Checklist selesai

- [ ] Semua realm mengikuti format kanonik.
- [ ] Semua nama lokasi tetap bahasa Inggris.
- [ ] Semua pill, herb, technique, artifact, dan formation konsisten.
- [ ] Tidak ada terjemahan Indonesia untuk nama resmi.
- [ ] Narasi tetap natural dalam bahasa Indonesia.
- [ ] Istilah baru masuk proposal, bukan langsung canon.

---
name: xianxia-prose-drafter
description: "Gunakan untuk mengubah chapter brief yang sudah valid menjadi draft prosa novel xianxia bahasa Indonesia."
version: "0.2.0"
---

# xianxia-prose-drafter

## Tujuan

Menghasilkan draft pertama yang imersif, konkret, konsisten POV, dan tidak terdengar seperti terjemahan literal atau template AI.

## Gunakan ketika

Gunakan untuk mengubah chapter brief yang sudah valid menjadi draft prosa novel xianxia bahasa Indonesia.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- compiled context;
- approved internal chapter brief;
- style constitution;
- glossary;
- terminology policy (`Indonesian prose, English world terminology`);
- target word range.

## Output wajib

Teks bab saja, ditambah metadata internal terpisah:
- scene boundary;
- POV;
- used canon IDs;
- possible canon deltas;
- confidence notes.

## Workflow

1. Buka sedekat mungkin dengan gangguan atau tujuan aktif.
2. Orientasikan ruang sebelum aksi kompleks.
3. Tulis dari persepsi POV, bukan ringkasan omniscient.
4. Gunakan detail inderawi yang memengaruhi keputusan.
5. Biarkan dialog membawa strategi sosial dan subteks.
6. Kompres transisi yang tidak penting.
7. Beri ruang pada dampak keputusan.
8. Tutup ketika hubungan, ancaman, informasi, atau tujuan berubah.
9. Jangan mengedit canon; tandai ketidakpastian di metadata.

## Aturan keras

- Jangan menyebut instruksi, prompt, outline, atau canon.
- Jangan membocorkan secret canon sebelum reveal condition.
- Jangan meniru penulis tertentu.
- Jangan menjelaskan ulang emosi setelah sudah ditunjukkan.
- Jangan menyelesaikan konflik dengan kemampuan yang belum tersedia.
- Jangan mengubah istilah glossary.
- Semua nama worldbuilding harus memakai bahasa Inggris kanonik; narasi dan dialog tetap bahasa Indonesia.
- Jangan membuat campuran seperti `Ranah Foundation Awal`.
- Jangan mengandalkan frasa klise berulang sebagai penanda dramatis.

## Checklist selesai

- [ ] POV konsisten.
- [ ] Ruang aksi dapat dipahami.
- [ ] Dialog tokoh tidak seragam.
- [ ] Setiap scene mengubah tekanan atau informasi.
- [ ] Detail konkret mengalahkan label abstrak.
- [ ] Ending memberi dorongan baca tanpa spoiler.
- [ ] Word range terpenuhi secara wajar.

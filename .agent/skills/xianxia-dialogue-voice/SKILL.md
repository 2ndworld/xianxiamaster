---
name: xianxia-dialogue-voice
description: "Gunakan setelah draft untuk memperkuat suara dialog, subteks, status sosial, dan batas pengetahuan setiap karakter tanpa mengubah kejadian."
version: "0.2.0"
---

# xianxia-dialogue-voice

## Tujuan

Mencegah semua tokoh terdengar seperti satu AI serta mencegah dialog eksposisi yang tidak alami.

## Gunakan ketika

Gunakan setelah draft untuk memperkuat suara dialog, subteks, status sosial, dan batas pengetahuan setiap karakter tanpa mengubah kejadian.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- draft;
- character voice cards;
- relationship state;
- knowledge boundaries;
- scene objective.

## Output wajib

Draft dengan revisi dialog terbatas dan laporan:
- changed lines;
- voice distinction;
- knowledge violations;
- exposition removed;
- unresolved issues.

## Workflow

1. Petakan tujuan sosial tiap pembicara.
2. Periksa apa yang diketahui, diduga, dan disembunyikan.
3. Bedakan sintaks, tingkat formalitas, metafora, dan kebiasaan menghindar.
4. Ubah eksposisi menjadi tekanan, tawar-menawar, pertanyaan, atau tindakan bila memungkinkan.
5. Pertahankan makna dan state change.
6. Tandai bila masalah sebenarnya berasal dari scene design, bukan dialog.

## Aturan keras

- Jangan memberi tokoh informasi di luar knowledge state.
- Jangan menjadikan aksen sebagai karikatur.
- Jangan menambahkan catchphrase ke setiap baris.
- Jangan mengubah keputusan plot.
- Jangan membuat semua dialog samar; kejelasan tetap penting.

## Checklist selesai

- [ ] Pembicara dapat dibedakan tanpa dialogue tag pada sampel.
- [ ] Dialog memiliki tujuan sosial.
- [ ] Tidak ada “seperti yang kau tahu” tanpa alasan.
- [ ] Status dan hubungan memengaruhi pilihan kata.
- [ ] Tidak ada knowledge leak.

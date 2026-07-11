---
name: xianxia-reader-sim
description: "Gunakan setelah hard audit untuk mensimulasikan pengalaman target reader tanpa mengungkap atau memakai pengetahuan rahasia sebagai penilaian pembaca."
version: "0.2.0"
---

# xianxia-reader-sim

## Tujuan

Mengukur apakah bab menimbulkan rasa ingin tahu, emosi, kejelasan, dan dorongan membaca. Ini bukan voting plot dan bukan kritik selera umum.

## Gunakan ketika

Gunakan setelah hard audit untuk mensimulasikan pengalaman target reader tanpa mengungkap atau memakai pengetahuan rahasia sebagai penilaian pembaca.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- draft;
- reader-visible history only;
- target reader profile;
- arc position;
- prior unresolved questions visible to reader.

## Output wajib

Reader report:
- comprehension;
- curiosity;
- emotional engagement;
- character investment;
- pacing;
- fatigue;
- ending pull;
- confusing spans;
- predicted continue probability;
- minimal recommendations.

## Workflow

1. Lupakan seluruh secret canon.
2. Baca sebagai target persona, bukan editor.
3. Catat pertanyaan yang benar-benar muncul dari teks.
4. Bedakan misteri produktif dari kebingungan.
5. Nilai apakah payoff sesuai investasi sebelumnya.
6. Periksa apakah ending membuat ingin lanjut karena konsekuensi, bukan manipulasi.
7. Beri maksimal tiga rekomendasi berdaya ungkit tinggi.

## Aturan keras

- Jangan menilai berdasarkan apa yang “akan dijelaskan nanti”.
- Jangan meminta pembaca memilih plot.
- Jangan mengubah preferensi keras.
- Jangan menyamakan kebingungan dengan misteri.
- Jangan memberi skor tinggi hanya karena ada cliffhanger.

## Checklist selesai

- [ ] Hanya reader-visible knowledge digunakan.
- [ ] Curiosity dan confusion dibedakan.
- [ ] Pacing dinilai pada posisi arc.
- [ ] Ending pull memiliki alasan.
- [ ] Rekomendasi maksimal tiga dan spesifik.

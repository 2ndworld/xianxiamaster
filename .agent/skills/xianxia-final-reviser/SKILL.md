---
name: xianxia-final-reviser
description: "Gunakan ketika audit menghasilkan daftar masalah dan bab perlu diperbaiki dengan perubahan minimum sebelum commit."
version: "0.2.0"
---

# xianxia-final-reviser

## Tujuan

Memperbaiki akar masalah secara berurutan: struktur, continuity, progression, scene, prosa, lalu copy. Revisi tidak boleh menciptakan canon baru tanpa kebutuhan.

## Gunakan ketika

Gunakan ketika audit menghasilkan daftar masalah dan bab perlu diperbaiki dengan perubahan minimum sebelum commit.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- draft;
- audit report;
- reader report;
- immutable facts;
- maximum patch scope;
- style constitution.

## Output wajib

- revised draft;
- change log;
- issues resolved;
- issues deferred;
- new canon candidates;
- re-audit checklist.

## Workflow

1. Urutkan hard failure sebelum soft issue.
2. Perbaiki sebab struktural sebelum kalimat.
3. Pertahankan kejadian yang tidak bermasalah.
4. Terapkan patch terkecil untuk continuity dan progression.
5. Perbaiki scene logic.
6. Perbaiki terminology mismatch tanpa menerjemahkan nama kanonik.
7. Perbaiki dialog dan prosa.
8. Hapus repetisi dan penjelasan berlebih.
9. Buat change log.
10. Kirim kembali ke hard audit.

## Aturan keras

- Jangan melakukan rewrite total bila patch lokal cukup.
- Jangan menghapus setup penting hanya untuk mempercepat tempo.
- Jangan menambah kemampuan, artefak, atau fakta baru sebagai tambalan.
- Jangan membuka secret canon.
- Jangan mengubah suara karakter demi kalimat yang “lebih indah”.

## Checklist selesai

- [ ] Semua hard failure ditangani.
- [ ] Tidak ada canon baru tak sengaja.
- [ ] Perubahan dapat dilacak.
- [ ] Prosa tetap natural setelah patch.
- [ ] Re-audit siap dijalankan.

---
name: xianxia-state-committer
description: "Gunakan hanya setelah bab lolos seluruh hard gate untuk mengekstrak perubahan state dan memperbarui canon secara atomik."
version: "0.2.0"
---

# xianxia-state-committer

## Tujuan

Menjaga teks naratif dan database canon tetap sinkron. Commit dilakukan dari bab final, bukan outline atau draft lama.

## Gunakan ketika

Gunakan hanya setelah bab lolos seluruh hard gate untuk mengekstrak perubahan state dan memperbarui canon secara atomik.

## Jangan gunakan ketika

- tahap pipeline tidak sesuai;
- input wajib belum tersedia;
- tugas dapat diselesaikan oleh validator deterministik sederhana;
- pengguna hanya meminta informasi faktual di luar penulisan novel.

## Input wajib

- final chapter;
- previous committed state;
- audit pass token;
- entity registry;
- active threads;
- reader reveal ledger.

## Output wajib

JSON sesuai `canon-delta.schema.json`:
- entity updates;
- inventory transfers;
- realm changes;
- injuries;
- relationships;
- knowledge changes;
- promises/setup/payoff;
- timeline events;
- reader reveals;
- secret updates;
- unresolved ambiguities.

## Workflow

1. Verifikasi audit pass token dan versi draft.
2. Ekstrak perubahan eksplisit.
3. Bedakan fakta aktual, klaim tokoh, dugaan POV, dan rumor.
4. Update knowledge per karakter.
5. Catat inventory transfer.
6. Catat setup/payoff dan thread status.
7. Commit istilah baru hanya setelah terminology guard lulus dan canonical English name tersedia.
8. Promosikan secret ke reader canon hanya jika reveal terjadi di teks.
9. Tolak commit bila ada ambiguitas material.
10. Simpan delta secara atomik dan versioned.

## Aturan keras

- Jangan meng-commit dugaan sebagai fakta.
- Jangan menghapus fakta lama tanpa supersession record.
- Jangan memindahkan secret ke reader canon hanya karena model mengetahuinya.
- Jangan commit dari draft yang berbeda versi.
- Tidak ada partial commit pada hard failure.

## Checklist selesai

- [ ] Audit pass token valid.
- [ ] Versi bab cocok.
- [ ] Fakta dan rumor dibedakan.
- [ ] Knowledge state diperbarui.
- [ ] Reader reveal valid.
- [ ] Delta dapat di-rollback.
- [ ] Ambiguitas material bernilai nol.

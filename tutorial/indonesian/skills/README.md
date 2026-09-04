# Tutorial Per Skill

Indeks ini mencakup seluruh skill yang tersedia di `.agents/skills/`. Pilih skill yang paling langsung memiliki pekerjaan; tambahkan skill lain hanya ketika tugas memang melintasi batas tanggung jawab.

| Skill | Gunakan untuk | Panduan |
| --- | --- | --- |
| `unslop-accessibility` | Semantik, keyboard, fokus, kontras, status, dan zoom | [Buka](unslop-accessibility/README.md) |
| `unslop-comments` | Audit atau perapian komentar tanpa mengubah perilaku kode | [Buka](unslop-comments/README.md) |
| `unslop-copy` | Teks produk dan pemasaran yang terlihat pengguna | [Buka](unslop-copy/README.md) |
| `unslop-docs` | Bootstrap, sinkronisasi, rekonstruksi, dan handoff dokumentasi | [Buka](unslop-docs/README.md) |
| `unslop-lean` | Solusi paling kecil yang tetap lengkap dan benar | [Buka](unslop-lean/README.md) |
| `unslop-logic` | API, state, data, validasi, dan aturan bisnis | [Buka](unslop-logic/README.md) |
| `unslop-responsive` | Reflow, overflow, navigasi adaptif, dan target sentuh | [Buka](unslop-responsive/README.md) |
| `unslop-ui` | Membangun atau memperbaiki antarmuka produk | [Buka](unslop-ui/README.md) |
| `unslop-ui-audit` | Audit visual read-only dengan temuan terprioritas | [Buka](unslop-ui-audit/README.md) |

## Cara memanggil

Pemanggilan eksplisit cocok ketika skill tertentu wajib dipakai:

```text
$unslop-responsive Perbaiki layout halaman katalog pada viewport sempit.
```

Untuk routing implisit, jelaskan tujuan dan batas tugas secara konkret. Codex memilih skill berdasarkan deskripsinya. Jangan memanggil seluruh skill sekaligus; lihat [panduan kombinasi](../07-combine-skills.md).

Tutorial adalah panduan untuk pengguna. Perilaku runtime tetap ditentukan oleh `AGENTS.md` dan masing-masing `SKILL.md`.

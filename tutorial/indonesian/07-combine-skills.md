# 07 — Menggabungkan Skills

Gabungkan skills berdasarkan concern yang benar-benar ada, bukan berdasarkan jumlah file yang disentuh.

## Kombinasi umum

| Tugas | Skill utama | Tambahan bila relevan |
|---|---|---|
| Membuat halaman baru | `unslop-ui` | `unslop-responsive`, `unslop-accessibility`, `unslop-copy` |
| Audit visual read-only | `unslop-ui-audit` | `unslop-accessibility` jika diminta |
| Fitur full-stack | `unslop-logic` + `unslop-ui` | `unslop-docs` jika pengetahuan durable berubah |
| Perbaikan layout mobile | `unslop-responsive` | `unslop-accessibility` untuk keyboard/touch/focus |
| Penyederhanaan implementasi | `unslop-lean` | `unslop-logic` bila behavior ikut dianalisis |
| Cleanup komentar | `unslop-comments` | Tidak perlu skill UI atau logic |
| Dokumentasi maintenance | `unslop-docs` | Skill domain hanya jika perlu memahami perubahan terkait |

## Contoh prompt gabungan

```text
$unslop-ui $unslop-responsive

Implementasikan ulang header checkout agar hierarchy lebih jelas dan
navigation tetap dapat digunakan pada layar sempit. Pertahankan routes,
design tokens, dan checkout behavior yang ada.
```

```text
$unslop-logic $unslop-docs

Tambahkan idempotency pada webhook pembayaran dengan test yang relevan.
Setelah terverifikasi, perbarui hanya dokumentasi arsitektur dan keputusan
yang berubah karena mekanisme tersebut.
```

## Hindari konflik mode

Jangan menggabungkan `unslop-ui-audit` yang read-only dengan prompt yang meminta implementasi langsung. Pilih audit terlebih dahulu atau gunakan `unslop-ui` untuk perubahan yang sudah diputuskan.

# 01 — Instal Unslop ke Proyek

## Tujuan

Membuat `AGENTS.md` dan seluruh skill Unslop tersedia di repository target.

## Struktur tujuan

```text
project/
|-- AGENTS.md
`-- .agents/
    `-- skills/
        |-- unslop-ui/
        |-- unslop-docs/
        `-- ...
```

## Langkah

1. Salin folder `.agents/` dari paket Unslop ke root repository target.
2. Jika proyek belum memiliki `AGENTS.md`, salin `AGENTS.md` dari paket.
3. Jika proyek sudah memiliki `AGENTS.md`, gabungkan baseline Unslop tanpa menghapus command, aturan domain, atau struktur proyek yang sudah ada.
4. Buka Codex dari root repository atau salah satu subfolder di dalam repository tersebut.
5. Periksa daftar skills atau coba pemanggilan eksplisit:

```text
$unslop-docs Jelaskan mode yang tersedia tanpa mengubah file.
```

## Jangan lakukan

- Jangan menaruh `.agents/skills` di child directory yang tidak berada pada jalur dari working directory ke repository root.
- Jangan mengganti `AGENTS.md` proyek secara buta.
- Jangan mengubah `SKILL.md` menjadi `skill.md`; entrypoint menggunakan huruf kapital.

## Hasil yang diharapkan

Codex dapat menemukan skill bernama `unslop-*`, dan baseline proyek dibaca sebelum agent mulai bekerja.

Untuk instalasi user-level, lihat `../INSTALL.md`.

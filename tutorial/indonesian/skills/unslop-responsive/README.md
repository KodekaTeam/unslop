# Menggunakan `unslop-responsive`

Skill ini memperbaiki cara UI beradaptasi terhadap ruang: reflow, overflow, navigasi, urutan konten, breakpoint berbasis konten, zoom, dan target sentuh.

## Kapan dipakai

Gunakan ketika layout pecah, konten terpotong, tabel tidak dapat digunakan, navigasi terlalu padat, atau komponen hanya dikecilkan tanpa recomposition. Jangan gunakan untuk redesign visual menyeluruh jika masalah utamanya bukan responsivitas.

## Alur kerja

1. Reproduksi kegagalan pada viewport dan konten nyata.
2. Temukan pemilik width, overflow, min-content, atau constraint yang menyebabkan masalah.
3. Recompose berdasarkan prioritas konten; jangan sekadar mengecilkan semua elemen.
4. Buat scroll lokal hanya pada area yang memang membutuhkannya.
5. Uji viewport lebar, sekitar breakpoint, sempit, zoom, teks panjang, sentuhan, dan keyboard.

## Contoh prompt

```text
$unslop-responsive Perbaiki dashboard ini pada lebar 320-768px. Prioritaskan reflow dan jangan sembunyikan aksi utama.
```

```text
$unslop-responsive Buat tabel transaksi tetap dapat digunakan di mobile dengan scroll lokal dan header yang jelas.
```

## Kombinasi yang sesuai

- Dengan `unslop-ui` untuk pembangunan atau redesign halaman.
- Dengan `unslop-accessibility` untuk zoom, keyboard, urutan baca, dan ukuran target.
- Dengan `unslop-copy` jika panjang teks nyata menjadi bagian dari pengujian layout.

## Hasil yang perlu diperiksa

Tidak boleh ada horizontal scroll pada halaman kecuali memang disengaja; konten penting tetap tersedia; target sentuh tidak terlalu kecil; urutan fokus dan baca tetap masuk akal. Breakpoint harus muncul karena kebutuhan konten, bukan kebiasaan angka perangkat.

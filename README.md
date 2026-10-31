# MGPA Event Calendar — Mockup v2

Mockup redesign halaman Events Calendar untuk [themandalikagp.com](https://www.themandalikagp.com).
Static single-page, semua CSS & JS inline di `index.html`.

## Struktur

```
index.html          # halaman utama (HTML + CSS + JS inline)
img/                # 15 gambar, sudah divendor
fonts/              # Roboto & Roboto Condensed (latin + latin-ext)
  fonts.css
  files/*.woff2
_headers            # security & cache header untuk Cloudflare Pages
wrangler.toml       # config Pages
```

## Deploy

Tidak ada build step. Cloudflare Pages setting:

- Framework preset: **None**
- Build command: *(kosong)*
- Build output directory: `/`

Atau lewat CLI:

```bash
npx wrangler pages deploy . --project-name mgpa-event-calendar
```

## Catatan asset

Gambar dan font sebelumnya di-hotlink dari `themandalikagp.com`, `cdn.themandalikagp.com`,
`jahada.themandalikagp.com`, `awsimages.detik.net.id`, dan `fonts.googleapis.com`.
Semuanya sudah diunduh dan di-commit ke repo, jadi halaman ini **nol dependency eksternal** —
render penuh tanpa koneksi keluar.

Untuk update gambar, taruh file baru di `img/` lalu ubah path di objek `P` (sekitar baris 1505
di `index.html`).

## Lisensi font

Roboto & Roboto Condensed — Apache License 2.0.

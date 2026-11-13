# WATERWAYS Final Pitch (GitHub Pages)

Deck pitching WATERWAYS (tim Ayam Renang, MAGE 12), 16 slide beranimasi dengan video gameplay.

## Isi folder

| File | Fungsi |
|---|---|
| `index.html` | Deck lengkap (font, gambar, dan catatan pembicara sudah tertanam) |
| `v/*.mp4` | 7 video gameplay yang diputar di slide |
| `vendor/gsap.min.js` | Library animasi GSAP 3.12.5, disimpan lokal supaya tidak bergantung CDN |
| `favicon.png` | Ikon tab browser |
| `.nojekyll` | Supaya GitHub Pages menyajikan file apa adanya |

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (misalnya `waterways-pitch`), pilih **Public**.
2. Upload **semua isi folder ini** ke root repository, termasuk folder `v/` dan `vendor/`.
   - Lewat web: tombol **Add file → Upload files**, seret semua file dan folder, lalu **Commit changes**.
   - Lewat terminal di folder ini:
     ```bash
     git init
     git add .
     git commit -m "Deploy WATERWAYS pitch deck"
     git branch -M main
     git remote add origin https://github.com/<username>/waterways-pitch.git
     git push -u origin main
     ```
3. Di repository: **Settings → Pages → Build and deployment**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1–2 menit. Deck tersedia di `https://<username>.github.io/waterways-pitch/`.

## Kontrol saat presentasi

- **→ / Spasi / Enter / klik**: langkah atau slide berikutnya
- **← / Backspace**: kembali
- **F**: layar penuh
- **N**: tampilkan catatan pembicara (dengan timer)
- **M**: mode ringan (animasi dikurangi, untuk laptop lambat)
- **H** atau **?**: bantuan tombol

## Coba lokal sebelum deploy

Video tidak diputar kalau `index.html` dibuka langsung dengan double-click dari beberapa browser. Jalankan server kecil di folder ini:

```bash
python -m http.server 8000
```

lalu buka `http://localhost:8000`.

# Citation Style APA 7th "dkk" untuk Mendeley Desktop

Gaya sitasi APA 7th yang mengganti "et al." menjadi "dkk." pada sitasi di Microsoft Word lewat plugin Mendeley Desktop.

Contoh hasil:

- Sebelum: (Smith et al., 2020)
- Sesudah: (Smith dkk., 2020)

## Isi Repositori

```
├── README.md
├── apa-dkk.csl      # gaya sitasi yang sudah diedit
└── original/
    └── apa.csl      # file asli, belum diedit
```

## Cara Memasang

1. Download file [apa-dkk.csl](apa-dkk.csl). Klik tombol **Download raw file** di GitHub.
2. Tutup Mendeley Desktop.
3. Buka folder berikut di File Explorer:
   `C:\Users\NAMA_ANDA\AppData\Local\Mendeley Ltd\Mendeley Desktop\citationStyles-1.0\`
   Ganti `NAMA_ANDA` dengan nama pengguna Windows Anda. Folder `AppData` tersembunyi. Aktifkan **View → Hidden items** di File Explorer jika tidak terlihat.
4. Salin `apa-dkk.csl` ke subfolder tersebut.
5. Buka Mendeley Desktop. Pilih **View → Citation Style → APA Style 7th edition - dkk**.
6. Buka Microsoft Word. Pilih tab **Mendeley → Style → APA Style 7th edition - dkk**, lalu klik **Refresh**.
7. Lakukan sitasi ulang. Tulisan "et al." berubah menjadi "dkk."

## Jika Gagal

- Gaya tidak muncul di daftar: pastikan file ada di subfolder yang benar (langkah 4), lalu buka ulang Mendeley Desktop.
- Gaya muncul di Mendeley, tidak muncul di Word: pasang ulang plugin Word.
  1. Di Mendeley Desktop, pilih **Tools → Uninstall MS Word Plugin**.
  2. Tutup Word.
  3. Pilih **Tools → Install MS Word Plugin**.
- Sitasi lama belum berubah: klik **Refresh** di tab Mendeley pada Word.

## Cara Membuat Sendiri untuk Gaya Lain

Metode ini bisa dipakai untuk gaya sitasi apa pun, tidak hanya APA.

1. Download file `.csl` gaya yang diinginkan dari [repositori CSL](https://github.com/citation-style-language/styles).
2. Buka file dengan Notepad atau editor teks (VS Code atau Antigravity).
3. Cari tag penutup `</info>`. Tepat di bawahnya, tambahkan:

   ```xml
   <locale xml:lang="en">
     <terms>
       <term name="et-al">dkk.</term>
     </terms>
   </locale>
   ```

4. Jika file sudah punya blok `<locale xml:lang="en">`, tambahkan hanya baris `<term name="et-al">dkk.</term>` ke dalam `<terms>` yang ada. Jangan buat blok ganda.
5. Di dalam `<info>`, ubah `<title>` dan `<id>` agar berbeda dari gaya asli. Contoh:
   - `<title>APA 7th dkk</title>`
   - `<id>http://www.zotero.org/styles/apa-dkk</id>`

   Jika `<id>` sama dengan gaya asli, Mendeley bisa mengabaikan file baru.
6. Simpan, lalu ikuti bagian **Cara Memasang** di atas.

Catatan:

- Jika gaya memakai bahasa lain (`default-locale="id-ID"`), ganti `xml:lang="en"` menjadi `xml:lang="id"`.
- Untuk hasil tanpa titik, tulis `dkk` saja.

## Catatan

- Diuji pada: Mendeley Desktop versi `1.19.8` dan Microsoft Word `MS WORD 2021`.
- Mendeley Desktop sudah tidak dikembangkan lagi oleh Elsevier. Pengganti resminya adalah Mendeley Reference Manager.

## Lisensi dan Kredit

Gaya sitasi ini diturunkan dari `apa.csl` di [Citation Style Language styles](https://github.com/citation-style-language/styles). Lisensi file CSL mengikuti **Creative Commons Attribution-ShareAlike 3.0** (CC BY-SA 3.0). Daftar penulis asli ada di blok `<contributor>` pada file `.csl`. Jangan hapus blok `<contributor>` dan `<rights>`.

Perubahan dari file asli: menambahkan istilah `et-al` dengan nilai `dkk.`, serta mengubah `<title>` dan `<id>`.

Karena CC BY-SA 3.0 bersifat share-alike, file turunan harus dibagikan dengan lisensi yang sama.

## Terima Kasih

Terima kasih kepada kontributor Citation Style Language yang menyediakan gaya sitasi secara terbuka.

# Citation Style Language untuk Format PPKI IPB

Download CSL: [https://ipb.link/csl](https://auriza.github.io/csl-ipb/ipb.csl)


## Panduan instalasi

### Mendeley

- Pada Mendeley Desktop, masuk ke menu "View", "Citation Style", "More Styles..."
- Masuk ke tab "Get More Styles", "Download Style", isikan link [https://ipb.link/csl](https://ipb.link/csl), klik "Download"

### Zotero

- Unduh [https://ipb.link/csl](https://ipb.link/csl), simpan dengan nama file `ipb.csl`.
- Masuk ke menu "Edit", "Preferences", "Cite", "Styles", klik tombol "+", dan pilih file `ipb.csl` yang sudah diunduh

## Penyesuaian metadata pustaka (Zotero)

| Komponen                  | Penulisan                                                             |
|:--------------------------|:----------------------------------------------------------------------|
| Judul buku                | *title case*                                                          |
| Nama jurnal/prosiding     | *title case*                                                          |
| Judul artikel             | *sentence case*                                                       |
| Judul cetak miring        | `<i>`*Oryza sativa*`</i>`                                             |
| **Artikel jurnal**        |                                                                       |
| - singkatan jurnal        | pada atribut `journal abbr`                                           |
| - penulis tidak ada       | pada atribut `short title` isikan kata pertama dari judul             |
| - penulis organisasi      | langsung singkatannya saja, belum didukung 🔴                          |
| - jenis artikel: editorial, ulasan, … | pada atribut `extra`/`note`                               |
| - sisipan, edisi khusus   | pada atribut `issue`                                                  |
| - judul artikel terjemah Inggris | pada atribut `extra`/`note`                                    |
| - artikel cetak ulang     | belum didukung 🔴                                                      |
| - artikel belum terbit    | kosongkan atribut `volume` dan `issue`                                |
| - artikel dari internet   | pada atribut `accessed`, tanggal akses seharusnya tidak diperlukan 🔴  |
| **Buku**                  |                                                                       |
| - kode negara bagian US   | pada atribut `place`                                                  |
| - buku dengan editor      | pada atribut `editor`                                                 |
| - buku dengan penerjemah  | pada atribut `translator`                                             |
| - penulis organisasi      | langsung singkatannya saja, belum didukung 🔴                          |
| - buku berseri judul volume sama  | pada atribut `volume`                                         |
| - buku berseri judul volume beda  | pada atribut `volume` tambahkan judul volumenya (nomor: judul)|
| - artikel dalam buku      | gunakan tipe `book section`                                           |
| **Prosiding**             |                                                                       |
| - tanggal konferensi      | pada atribut `extra`/`note` tambahkan isian `Event Date: YYYY-MM-DD/YYYY-MM-DD` |
| - tempat konferensi       | kosongkan atribut `place` dan pada atribut `extra`/`note` tambahkan isian `Event Place:` dan `Publisher Place:` |
| - artikel dari internet   | pada atribut `URL` dan `accessed`                                      |
| - nomor abstrak           | belum didukung 🔴                                                      |
| **Tesis**                 |                                                                       |
| - jenis: skripsi, tesis, disertasi | pada atribut `type`                                          |



## Pengujian

Masukan:

- daftar pustaka: [YAML](https://auriza.github.io/csl-ipb/test/ppki4.yaml), [BibTeX](https://auriza.github.io/csl-ipb/test/ppki4.bib)
- halaman uji: [Markdown](https://auriza.github.io/csl-ipb/test/ppki4.md)

Keluaran: [HTML](https://auriza.github.io/csl-ipb/test/ppki4.html), [PDF](https://auriza.github.io/csl-ipb/test/ppki4.pdf)

<!-- Contoh paper: [HTML](https://auriza.github.io/csl-ipb/tesis/paper.html), [PDF](https://auriza.github.io/csl-ipb/tesis/paper.pdf) -->

Pengujian dilakukan dengan mengekspor koleksi pustaka dari Zotero dengan format "Better CSL YAML"
dan mengkompilasi halaman uji dengan `pandoc`.

![CSL dalam ekosistem penulisan pustaka](csl.png)

# Citation Style Language untuk Format PPKI IPB

Download CSL: [https://ipb.link/csl](https://auriza.github.io/csl-ipb/ipb.csl)

![CSL dalam ekosistem penulisan pustaka](csl.png)

## Penyesuaian metadata pustaka pada Zotero

| Komponen                  | Penulisan                                                             |
|:--------------------------|:----------------------------------------------------------------------|
| Judul buku                | *title case*                                                          |
| Nama jurnal/prosiding     | *title case*                                                          |
| Judul artikel             | *sentence case*                                                       |
| Judul cetak miring        | `<i>`*Oryza sativa*`</i>`                                             |
| **Artikel jurnal**        |                                                                       |
| - singkatan jurnal        | pada atribut `journal abbr`                                           |
| - penulis tidak ada       | pada atribut `short title`: kata pertama dari judul                   |
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
| - buku berseri judul volume sama  | pada atribut `volume` |
| - buku berseri judul volume beda  | pada atribut `volume` tambahkan judul volumenya (nomor: judul)|
| - artikel dalam buku      | gunakan tipe `book section` |




## Contoh Keluaran

Hasil uji coba: [HTML](https://auriza.github.io/csl-ipb/test/ppki4.html), [PDF](https://auriza.github.io/csl-ipb/test/ppki4.pdf)

Contoh paper: [HTML](https://auriza.github.io/csl-ipb/tesis/paper.html), [PDF](https://auriza.github.io/csl-ipb/tesis/paper.pdf)

Catatan: untuk kompilasi dengan Pandoc, ekspor koleksi dari Zotero dengan format BibTex, bukan BibLaTeX.

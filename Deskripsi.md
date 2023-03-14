Data tersebut terkait dengan kampanye pemasaran langsung dari lembaga perbankan Portugis. Kampanye pemasaran didasarkan pada panggilan telepon. Seringkali, lebih dari satu kontak ke klien yang sama diperlukan, untuk mengakses apakah produk (deposit berjangka bank) akan ('ya') atau tidak ('tidak') berlangganan.

Ada empat dataset:
1) bank-additional-full.csv dengan semua contoh (41188) dan 20 input, diurutkan berdasarkan tanggal (dari Mei 2008 hingga November 2010), sangat dekat dengan data yang dianalisis dalam [Moro et al., 2014]
2) bank-additional.csv dengan 10% contoh (4119), dipilih secara acak dari 1), dan 20 masukan.
3) bank-full.csv dengan semua contoh dan 17 input, diurutkan berdasarkan tanggal (versi lama dari kumpulan data ini dengan input yang lebih sedikit).
4) bank.csv dengan 10% contoh dan 17 masukan, dipilih secara acak dari 3 (versi lama kumpulan data ini dengan masukan lebih sedikit).
Kumpulan data terkecil disediakan untuk menguji algoritme pembelajaran mesin yang lebih menuntut komputasi (mis., SVM).

Tujuan klasifikasi adalah untuk memprediksi apakah klien akan berlangganan (ya/tidak) deposito berjangka (variabel y).

Informasi Atribut:

Variabel masukan:
# data klien bank:
1 - usia (numerik)
2 - pekerjaan : jenis pekerjaan (kategori: 'admin.', 'kerah biru', 'pengusaha', 'pembantu rumah tangga', 'manajemen', 'pensiunan', 'wiraswasta', 'jasa', 'pelajar' ,'teknisi','pengangguran','tidak dikenal')
3 - perkawinan: status perkawinan (kategori: 'bercerai', 'menikah', 'lajang', 'tidak diketahui'; catatan: 'bercerai' berarti bercerai atau janda)
4 - pendidikan (kategori: 'basic.4y', 'basic.6y', 'basic.9y', 'high.school', 'illiterate', 'professional.course', 'university.degree', 'unknown')
5 - default: apakah kredit default? (kategori: 'tidak', 'ya', 'tidak diketahui')
6 - perumahan: memiliki pinjaman perumahan? (kategori: 'tidak', 'ya', 'tidak diketahui')
7 - pinjaman: memiliki pinjaman pribadi? (kategori: 'tidak', 'ya', 'tidak diketahui')
# terkait dengan kontak terakhir dari kampanye saat ini:
8 - kontak: jenis komunikasi kontak (kategori: 'seluler', 'telepon')
9 - bulan: kontak terakhir bulan dalam setahun (kategori: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
10 - day_of_week: hari kontak terakhir dalam seminggu (kategori: 'mon', 'tue', 'wed', 'thu', 'fri')
11 - durasi: durasi kontak terakhir, dalam detik (numerik). Catatan penting: atribut ini sangat memengaruhi target keluaran (misalnya, jika durasi=0 maka y='tidak'). Namun, durasinya tidak diketahui sebelum panggilan dilakukan. Juga, setelah akhir panggilan y jelas diketahui. Dengan demikian, input ini hanya boleh dimasukkan untuk tujuan pembandingan dan harus dibuang jika tujuannya adalah untuk mendapatkan model prediksi yang realistis.
# atribut lainnya:
12 - kampanye: jumlah kontak yang dilakukan selama kampanye ini dan untuk klien ini (numerik, termasuk kontak terakhir)
13 - pdays: jumlah hari yang berlalu setelah klien terakhir dihubungi dari kampanye sebelumnya (numerik; 999 berarti klien tidak dihubungi sebelumnya)
14 - sebelumnya: jumlah kontak yang dilakukan sebelum kampanye ini dan untuk klien ini (numerik)
15 - cemberut: hasil dari kampanye pemasaran sebelumnya (kategori: 'gagal', 'tidak ada', 'sukses')
# atribut konteks sosial dan ekonomi
16 - emp.var.rate: tingkat variasi pekerjaan - indikator triwulanan (numerik)
17 - cons.price.idx: indeks harga konsumen - indikator bulanan (numerik)
18 - cons.conf.idx: indeks kepercayaan konsumen - indikator bulanan (numerik)
19 - euribor3m: tarif 3 bulan euribor - indikator harian (numerik)
20 - nr.employed: jumlah karyawan - indikator triwulanan (numerik)

Variabel keluaran (target yang diinginkan):
21 - y - apakah klien sudah berlangganan term deposit? (biner: 'ya', 'tidak')


Makalah yang relevan:

S. Moro, P. Cortez dan P. Rita. Pendekatan Berbasis Data untuk Memprediksi Keberhasilan Telemarketing Bank. Sistem Pendukung Keputusan, Elsevier, 62:22-31, Juni 2014
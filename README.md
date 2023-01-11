# SIG-TEORI-Basic GIS operations
# Making a Map (QGIS3)
1.	Unduh dan ekstrak data Natural Earth Quick Start Kit. Buka QGIS. Temukan folder di panel Browser . Luaskan folder untuk menemukan proyek. Ini adalah file proyek yang berisi lapisan bergaya dalam format Dokumen QGIS. Klik dua kali proyek untuk membukanya.Natural Earth quick startNatural_Earth_quick_start_for_QGIS_v3
2.	Anda mungkin memperhatikan bahwa peta memiliki label dalam bahasa Yunani. Proyek ini menggunakan variabel untuk mengatur bahasa. Kita dapat mengubah variabel dengan masuk ke Project Properties .
3.	Beralih ke tab Variabel dalam dialog Properti Proyek . Cari project_languagevariabel dan klik pada kolom Nilai untuk mengeditnya. Ubah bahasa menjadi name_endan klik OK .
4.	Kembali ke jendela utama QGIS, klik tombol Refresh di Map Navigation Toolbar . Anda sekarang akan melihat peta yang dirender dengan label bahasa Inggris.
5.	Gunakan kontrol geser dan perbesar/perkecil di Bilah Alat Navigasi Peta dan perbesar ke Jepang.
6.	Anda dapat mematikan beberapa layer peta untuk data yang tidak kita perlukan untuk peta ini. Perluas folder dan hapus centang pada kotak di sebelah dan lapisan. Sebelum kita membuat peta yang cocok untuk dicetak, kita perlu memilih proyeksi yang sesuai. CRS default untuk proyek diatur ke . Ini adalah CRS yang populer digunakan untuk pemetaan web dan merupakan pilihan yang layak untuk tujuan kita, sehingga kita dapat menyerahkannya pada nilai defaltnya. Buka Proyek ‣ Tata Letak Cetak Baru .z5 - 1:18mne_10m_geography_marine_polysne_10m_admin_0_disputed_areasEPSG:3857 Pseudo-Mercator
7.	Anda akan diminta memasukkan judul untuk tata letak. Anda dapat membiarkannya kosong dan klik Ok .
8.	Di jendela Print Layout, klik tombol Zoom full untuk menampilkan Layout sepenuhnya.
9.	Sekarang kita harus membawa tampilan peta yang kita lihat di Kanvas QGIS ke tata letak. Pergi ke Tambah Item Tambah Peta .
10.	Setelah mode Tambahkan Peta aktif, tahan tombol kiri mouse dan seret persegi panjang tempat Anda ingin menyisipkan peta.
11.	Anda akan melihat bahwa jendela persegi panjang akan dirender dengan peta dari kanvas QGIS utama. Peta yang diberikan mungkin tidak mencakup seluruh wilayah minat kita. Gunakan opsi Edit ‣ Select/Move item dan Edit ‣ Move Content untuk menggeser peta di jendela dan memusatkannya di komposer.
12.	Mari kita juga sesuaikan tingkat zoom untuk peta. Klik pada tab Properti Barang dan masukkan 10000000sebagai nilai Skala .
13.	Sekarang kita akan menambahkan inset peta yang menunjukkan tampilan yang diperbesar untuk area Tokyo. Sebelum kita membuat perubahan pada lapisan di jendela utama QGIS, centang kotak Kunci lapisan dan Gaya kunci untuk lapisan . Ini akan memastikan bahwa jika kita mematikan beberapa lapisan atau mengubah gayanya, tampilan ini tidak akan berubah.
14.	Beralih ke jendela QGIS utama. Matikan grup layer dan aktifkan grup. Grup lapisan ini memiliki gaya yang lebih sesuai untuk tampilan yang diperbesar. Gunakan kontrol pan dan zoom di Map Navigation Toolbar dan zoom di sekitar Tokyo.z5 - 1:18mz7 - 1: 4m
15.	Kami sekarang siap untuk menambahkan inset peta. Ganti jendela Print Layout . Pergi ke Tambah Item Tambah Peta .
16.	Seret persegi panjang di tempat Anda ingin menambahkan sisipan peta. Anda sekarang akan melihat bahwa kita memiliki 2 objek peta di Print Layout. Saat membuat perubahan, pastikan Anda telah memilih peta yang benar.
17.	Pilih objek yang baru saja kita tambahkan dari panel Item . Pilih tab properti Item . Gulir ke bawah ke panel Bingkai dan centang kotak di sebelahnya. Anda dapat mengubah warna dan ketebalan batas bingkai sehingga mudah dibedakan dengan latar belakang peta.Map 2
18.	Salah satu fitur rapi dari Tata Letak Cetak adalah ia dapat secara otomatis menyorot area dari peta utama yang diwakili di sisipan. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Ikhtisar . Klik tombol Tambahkan ikhtisar baru .Map 1
19.	Pilih sebagai Bingkai Peta . Ini memberi tahu Print Layout untuk menyorot objek saat ini dengan luas peta yang ditampilkan di objek.Map 2Map 1Map 2
20.	Sekarang setelah inset peta siap, kita akan menambahkan kisi ke peta utama. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Kisi . Klik tombol Add a new grid , diikuti oleh Modify grid… .Map 1
21.	Secara default, garis kisi menggunakan unit dan proyeksi yang sama dengan proyeksi peta yang dipilih saat ini. Namun, lebih umum dan berguna untuk menampilkan garis kisi dalam derajat. Kita dapat memilih CRS yang berbeda untuk grid. Klik tombol Change… di sebelah CRS .
22.	Dalam dialog Pemilih Sistem Referensi Koordinat4326 , masukkan dalam kotak Filter . Dari hasil, pilih sebagai CRS. Klik Oke .WGS84 EPSG:4326
23.	Pilih nilai Interval sebagai 5derajat dalam arah X dan Y. Anda dapat menyesuaikan Offset untuk mengubah tempat munculnya garis grid.
24.	Gulir ke bawah ke bagian Bingkai kisi dan centang kotak Gambar koordinat . Format defaultnya adalah Degreestetapi muncul sebagai angka. Yang bisa kita sesuaikan adalah dengan menambahkan simbol °. Pilih Customdan klik tombol Ekspresi di sebelahnya.
25.	Masukkan ekspresi berikut untuk membuat string yang menggunakan nomor kisi dan menambahkan simbol ° ke dalamnya.
26.	Perhatikan bahwa kisi sekarang memiliki label khusus dari ekspresi. Sesuaikan pengaturan posisi untuk Left , Right , Top dan Bottom sesuai keinginan Anda.
27.	Sekarang kita akan menambahkan bingkai Persegi Panjang untuk menampung elemen peta lainnya seperti panah utara, skala, dan label. Pergi ke Tambahkan Item ‣ Tambahkan Bentuk ‣ Tambahkan Persegi Panjang .
28.	Anda dapat mengubah Gaya persegi panjang agar sesuai dengan latar belakang peta.
29.	Sekarang kita akan menambahkan Panah Utara ke peta. QGIS hadir dengan koleksi gambar terkait peta yang bagus - termasuk banyak jenis Panah Utara. Klik Tambah Barang ‣ Tambah Gambar .
30.	Tahan tombol kiri mouse Anda, gambar persegi panjang. Di panel sebelah kanan, klik tab Item Properties dan perluas bagian Cari direktori dan pilih gambar yang Anda sukai.
31.	Sekarang kita akan menambahkan bilah skala. Klik Tambahkan Item ‣ Tambahkan Bilah Skala 
32.	Klik pada tata letak tempat Anda ingin bilah skala muncul. Di tab Properti Item , pastikan Anda telah memilih elemen peta yang benar untuk menampilkan bilah skala. Pilih Gaya yang sesuai dengan kebutuhan Anda. Di panel Segmen , ubah Lebar tetap menjadi satuan dan sesuaikan segmen sesuai keinginan Anda.Map 1200
33.	Saatnya memberi label pada peta kita. Klik Tambah Barang ‣ Tambah Label .
34.	Klik pada peta dan gambar kotak tempat label seharusnya berada. Di tab Properti Barang , perluas bagian Label dan masukkan label untuk peta. Demikian pula, tambahkan label lain untuk kredit data dan perangkat lunak.
35.	Setelah puas dengan peta, Anda dapat mengekspornya sebagai Gambar, PDF, atau SVG. Untuk tutorial ini, mari ekspor sebagai gambar. Klik Tata Letak ‣ Ekspor sebagai Gambar .
36.	Simpan gambar dalam format yang Anda sukai. Di bawah ini adalah gambar PNG yang diekspor.

# Working with Attributes (QGIS3) (Project 2)
1.	Temukan ne_10m_populated_places_simple.zipfile di Peramban QGIS dan kembangkan. Pilih ne_10m_populated_places_simple.shpfile dan seret ke kanvas.
2.	Lapisan baru ne_10m_populated_places_simplesekarang akan dimuat di QGIS dan Anda akan melihat banyak titik yang mewakili tempat berpenduduk di dunia. Tampilan default di kanvas QGIS menunjukkan geometri layer GIS. Setiap titik juga memiliki atribut terkait. Mari kita lihat. Temukan Bilah Alat Atribut . Toolbar ini berisi banyak alat yang berguna untuk menginspeksi, melihat, memilih, dan memodifikasi atribut dari sebuah layer.
3.	Klik tombol Identifikasi pada Bilah Alat Atribut . Setelah alat dipilih, klik titik mana pun di kanvas. Atribut terkait dari titik itu akan ditampilkan di panel Identifikasi Hasil baru. Setelah Anda selesai menjelajahi atribut dari berbagai titik, Anda dapat mengklik tombol Tutup .
4.	Daripada melihat atribut satu fitur pada satu waktu, kita dapat melihat semuanya bersama-sama sebagai sebuah tabel. Klik tombol Open Attribute Table pada Attributes Toolbar . Anda juga dapat mengklik kanan ne_10m_populated_places_simplelayer dan memilih Open Attribute Table .
5.	Anda dapat menggulir secara horizontal dan menemukan kolom pop_max . Bidang ini berisi populasi tempat terkait. Anda dapat mengklik dua kali pada tajuk bidang untuk mengurutkan kolom dalam urutan menurun.
6.	Sekarang kami siap untuk melakukan kueri kami pada atribut ini. QGIS menggunakan ekspresi mirip SQL untuk melakukan kueri. Klik Pilih fitur menggunakan tombol ekspresi .
7.	Di jendela Select By Expression , perluas bagian Fields and Values dan klik dua kali pop_maxlabelnya. Anda akan melihat bahwa itu ditambahkan ke bagian ekspresi di bagian bawah. Jika Anda tidak yakin tentang nilai bidang, Anda dapat mengklik tombol Semua Unik untuk melihat nilai atribut apa yang ada dalam kumpulan data. Untuk latihan ini, kami mencari semua fitur yang memiliki populasi lebih dari 1 juta. Jadi lengkapi ekspresi seperti di bawah ini dan klik Select Features lalu Close .

"pop_max" > 1000000
8.	Anda akan melihat bahwa beberapa baris dalam tabel atribut sekarang dipilih. Jendela label juga berubah dan menunjukkan jumlah fitur yang dipilih.
9.	Tutup jendela tabel atribut dan kembali ke jendela utama QGIS. Anda akan melihat bahwa subset poin sekarang ditampilkan dengan warna kuning. Ini adalah hasil dari kueri kami dan titik yang dipilih adalah titik yang memiliki pop_maxnilai atribut lebih besar dari 1000000.
10.	Mari kita perbarui kueri kita dengan menyertakan syarat bahwa tempat itu juga harus menjadi ibu kota selain memiliki populasi lebih dari 1 juta. Untuk membuka editor ekspresi dengan cepat, Anda dapat menggunakan tombol Select Features by Expression di Attributes Toolbar .
11.	Bidang yang berisi data tentang huruf kapital adalah adm0cap . Nilai tersebut 1menunjukkan bahwa tempat tersebut adalah ibukota. Kita dapat menambahkan kriteria ini ke ekspresi kita sebelumnya menggunakan operator and . Masukkan ekspresi seperti di bawah ini dan klik Select Features lalu Close .
"pop_max" > 1000000 and "adm0cap" = 1
12.	Kembali ke jendela utama QGIS. Sekarang Anda akan melihat subset yang lebih kecil dari poin yang dipilih. Ini adalah hasil kueri kedua dan menampilkan semua tempat dari kumpulan data yang merupakan ibu kota negara serta memiliki populasi lebih dari 1 juta.
13.	Sekarang kita akan mengekspor fitur yang dipilih sebagai layer baru. Klik kanan ne_10m_populated_places_simplelayer dan pergi ke Export ‣ Save Selected Features As…
14.	Anda dapat memilih format apa pun yang Anda sukai sebagai Format . Untuk latihan ini, kita akan memilih GeoJSON. GeoJSON adalah format berbasis teks yang digunakan secara luas dalam pemetaan web. Klik tombol … di sebelah Nama file dan masukkan populated_capitals.geojsonsebagai file keluaran.
15.	Data input memiliki banyak kolom. Anda hanya dapat memilih sebagian dari kolom asli untuk diekspor. Luaskan bagian Pilih bidang untuk diekspor dan opsi ekspornya . Klik Batalkan Pilihan Semua dan centang kolom namedan pop_max. Klik Oke .
16.	Sebuah layer baru populated_capitalsakan dimuat di QGIS. Anda dapat menghapus centang pada ne_10m_populated_places_simplelayer untuk menyembunyikannya dan melihat poin dari layer yang baru diekspor.

# Importing Spreadsheets or CSV files (QGIS3) (Project 3)
1.	Periksa sumber data tabular Anda. Basis data gempa yang diunduh berisi Latitudedan Longitudebidang yang menunjukkan lokasi episentrum gempa dan atribut terkait lainnya. Kami akan menggunakan bidang ini untuk mengimpor file sebagai lapisan titik. Buka data dalam editor teks seperti Notepad/TextMate untuk melihat isinya. Anda akan melihat bahwa TAB memisahkan setiap bidang.
2.	QGIS hadir dengan pengelola data terpadu yang memungkinkan Anda memuat semua format data yang didukung. Klik tombol Buka Pengelola Sumber Data di Bilah Alat Sumber Data . Anda juga dapat menggunakan pintasan keyboard.Ctrl + L
3.	Dalam kotak dialog Pengelola Sumber Data , alihkan ke tab Teks Dibatasi . Klik tombol … di sebelah nama File .
4.	Bergantung pada sistem operasi, Anda mungkin atau mungkin tidak melihat file di lokasi yang diunduh. Dalam Format file, alihkan ke untuk melihat file tsv .All files (*; *.*)
5.	Sekarang Anda akan melihat file yang diunduh. Pilih itu dan klik Buka .
6.	Di kotak dialog Pengelola Sumber Data , jalur ke file akan tersedia di Nama File . Ubah nama Lapisan menjadi 1900_2000_earthquakes. Di bagian Format file , pilih Pembatas khusus dan centang Tab. Di bagian Definisi geometri , pilih Koordinat titik . Secara default , nilai bidang X dan bidang Y akan terisi secara otomatis jika menemukan bidang nama yang sesuai di input. Dalam kasus kami, mereka adalah Longitudedan Latitude. Anda dapat mengubahnya jika impor memilih bidang yang salah. Anda dapat membiarkan Geometry CRS ke defaultEPSG:4326 - WGS 84CRS. Jika file Anda berisi koordinat dalam CRS yang berbeda, Anda dapat memilih CRS yang sesuai di sini. Klik Tambahkan .
7.	Anda sekarang akan melihat bahwa data akan diimpor dan ditampilkan di kanvas QGIS sebagai layer baru yang disebut 1900_2000_earthquakesdengan CRS EPSG:4326.

# Basic Vector Styling (QGIS3)
1.	Buka zip kedua kumpulan data ke folder di komputer Anda. Di Panel Browser QGIS, temukan direktori tempat Anda mengekstrak data. Perluas ne_10m_landfolder dan pilih ne_10m_land.shplayer. Seret layer ke kanvas.
2.	Anda akan mendapatkan layer baru yang ne_10m_landditambahkan ke panel Layers . Database pembangkit listrik global hadir sebagai file CSV, jadi kita perlu mengimpornya. Klik tombol Buka
3.	Pengelola Sumber Data di Bilah Alat Sumber Data . Anda juga dapat menggunakan pintasan keyboard.Ctrl + L
4.	Di jendela Pengelola Sumber Data , alihkan ke tab Teks yang Dibatasi . Klik tombol … di sebelah Nama file dan ramban ke direktori tempat Anda mengekstrak globalpowerplantdatabasev120.zipfile. Pilih global_power_plant_database.csv. QGIS akan secara otomatis mendeteksi pembatas dan bidang geometri. Biarkan CRS Geometri ke nilai default . Klik Tambah diikuti oleh Tutup .EPSG:4326 - WGS84
5.	Lapisan baru global_power_plant_databaseakan ditambahkan ke panel Lapisan dan Anda akan melihat titik-titik yang mewakili pembangkit listrik di kanvas. Sekarang kita siap untuk memberi style pada kedua layer ini. Klik tombol panel Open the Layer Styling di bagian atas panel Layers .
6.	Panel Layer Styling akan terbuka di sebelah kanan. Pilih ne_10m_landlayer terlebih dahulu. Ini akan menjadi lapisan dasar kita sehingga kita bisa menjaga gaya minimalis agar tidak mengganggu. Klik dan gulir ke bawah. Pilih warna Isi sesuai keinginan Anda. Klik drop-down di sebelah warna Goresan dan pilih . Ini akan mengatur garis besar poligon tanah menjadi transparan. Anda akan melihat hasil seleksi Anda langsung diterapkan ke layer.Simple fillTransparent Stroke
7.	Selanjutnya pilih global_power_plant_databaselapisan. Klik dan gulir ke bawah. Pilih penanda segitiga.Simple marker
8.	Gulir ke atas dan pilih warna Isi sesuai keinginan Anda. Teknik kartografi yang berguna adalah memilih versi warna isian yang sedikit lebih gelap sebagai warna Stroke . Daripada mencoba memilihnya secara manual, QGIS menyediakan ekspresi untuk mengontrol ini dengan lebih tepat. Klik tombol Penimpaan yang ditentukan data dan pilih Edit .
9.	Masukkan ekspresi berikut untuk mengatur warnanya menjadi 30% lebih gelap dari warna isian dan klik OK .
10.	Anda akan melihat bahwa tombol Override yang ditentukan Data di sebelah Warna Stroke telah berubah menjadi kuning - menunjukkan bahwa properti ini dikendalikan oleh override. Render simbol tunggal dari lapisan pembangkit listrik tidak terlalu berguna. Itu tidak menyampaikan banyak informasi kecuali lokasi pembangkit listrik. Mari kita gunakan penyaji yang berbeda untuk membuatnya lebih berguna. Klik drop-down Symbology dan pilih Categorizedrenderer.
11.	Lapisan tersebut global_power_plant_databaseberisi atribut yang menunjukkan bahan bakar utama yang digunakan di setiap pembangkit listrik. Kita dapat membuat gaya di mana setiap jenis bahan bakar yang unik ditampilkan dalam warna yang berbeda. Pilih primary_fuelsebagai Kolom . Klik Klasifikasi . Anda akan melihat beberapa kategori dan rendering peta berubah sesuai.
12.	Meskipun tampilan Categorized berguna, lapisan ini berisi terlalu banyak kategori untuk ditafsirkan peta secara bermakna. Pendekatan yang lebih baik adalah mengelompokkan jenis kategori bahan bakar tertentu dan mengurangi jumlah kelas. Mari kita coba membuat 3 kategori - Bahan bakar terbarukan , Bahan bakar tidak terbarukan dan Lainnya . Pilih Rule-basedpenyaji. Pilih semua kecuali satu aturan dengan menahan Ctrltombol dan mengklik setiap baris. Setelah dipilih, klik tombol Hapus aturan yang dipilih untuk menghapusnya.
13.	Pilih aturan yang tersisa dan klik Edit aturan saat ini .
14.	Masukkan sebagai Label . Klik tombol Ekspresi di samping Filter .Renewable fuel
15.	Dalam dialog Pembuat String Ekspresi , masukkan ekspresi berikut dan klik OK . Di sini kami mengelompokkan beberapa kategori energi terbarukan ke dalam satu kategori.

"primary_fuel" IN ('Biomass', 'Geothermal', 'Hydro', 'Solar', 'Wind', 'Storage', 'Wave and Tidal')

16.	Gulir ke bawah dan klik Penanda sederhana . Pilih warna Isi yang sesuai . Setelah selesai, klik tombol Kembali .
17.	Anda akan melihat satu aturan diterapkan pada lapisan untuk kategori bahan bakar terbarukan . Klik kanan baris dan pilih Salin . Klik kanan lagi dan pilih Tempel .
18.	Salinan aturan yang ada akan ditambahkan. Pilih baris yang baru ditambahkan dan klik Edit aturan saat ini .
19.	Masukkan sebagai Label . Klik tombol Ekspresi di samping Filter .Non-renewable fuel
20.	Dalam dialog Pembuat String Ekspresi , masukkan ekspresi berikut dan klik OK .
"primary_fuel" IN ('Coal', 'Gas', 'Nuclear', 'Oil', 'Petcoke')
21.	Gulir ke bawah dan klik Penanda sederhana . Pilih warna Isi yang sesuai . Setelah selesai, klik tombol Kembali .
22.	Ulangi proses Salin/Tempel untuk menambahkan aturan ketiga. Pilih dan klik Edit aturan saat ini .
23.	Masukkan Othersebagai Label . Pilih Lain - Tangkap semua untuk fitur lain , bukan Filter . Ini akan memastikan bahwa setiap kategori yang terlewatkan dalam 2 aturan sebelumnya, akan diberi gaya oleh aturan ini. Gulir ke bawah dan klik Penanda sederhana . Pilih warna Isi yang sesuai . Setelah selesai, klik tombol Kembali .
24.	Pengkategorian ulang selesai sekarang. Anda akan melihat tampilan yang jauh lebih bersih yang menunjukkan distribusi sumber bahan bakar terbarukan vs. tidak terbarukan yang digunakan oleh pembangkit listrik dan distribusinya di seluruh negara. Namun ini tidak memberikan gambaran yang lengkap. Kita bisa menambahkan variabel lain ke styling. Daripada menampilkan semua penanda dengan ukuran seragam, kami dapat menunjukkan ukuran yang proporsional dengan kapasitas pembangkit listrik masing-masing pembangkit. Teknik kartografi ini disebut pemetaan Multivariat . Klik kanan aturan dan pilih Ubah Ukuran .Renewable fuel
25.	Klik tombol Penggantian yang ditentukan data di samping Ukuran . Pilih Sunting .
26.	Karena kapasitas pembangkit listrik sangat bervariasi di antara kumpulan data kami, cara efektif untuk mendapatkan rentang ukuran yang kecil adalah dengan menggunakan log10fungsi. Anda dapat bereksperimen dengan berbagai ekspresi untuk mendapatkan yang terbaik untuk visualisasi pilihan Anda. Masukkan ekspresi berikut dan klik OK .
log10("capacity_mw") + 1
27.	Ulangi proses yang sama untuk aturan lainnya.
28.	Setelah puas, Anda dapat menutup panel Layer Styling .
29.	Melihat visualisasi akhir kami, Anda dapat langsung melihat pola di dataset. Sebagai contoh, di Eropa terdapat lebih banyak pembangkit listrik yang menggunakan sumber energi terbarukan, tetapi kapasitasnya lebih rendah daripada pembangkit yang menggunakan sumber energi tidak terbarukan.

# Calculating Line Lengths and Statistics (QGIS3)
1.	Temukan ne_10m_railroads_north_america.zipfile yang diunduh di panel Browser dan perluas. Seret ne_10m_railroads_north_america.shpfile ke kanvas.
2.	Anda akan melihat layer baru ne_10m_railroads_north_americadimuat di panel Layers . Anda akan melihat bahwa layer tersebut memiliki garis yang mewakili rel kereta api untuk seluruh Amerika Utara. Sekarang, mari hitung panjang setiap fitur garis. Pergi ke Memproses ‣ Kotak Alat .
3.	Cari dan temukan geometri Vektor Tambahkan algoritma atribut geometri. Klik dua kali untuk meluncurkannya.
4.	Dalam dialog Add Geometry Attributesne_10m_railroads_north_america , pilih sebagai lapisan Input . Sistem Referensi Koordinat (CRS) lapisan input adalah EPSG:4326 WGS84 . Ini adalah CRS Geografis dengan Latitude dan Longitude sebagai koordinat, WGS84 sebagai ellipsoid dan derajat sebagai unit. Karena lintang dan bujur tidak memiliki panjang standar, Anda tidak dapat mengukur jarak atau area secara akurat menggunakan fungsi geometri planar. Untungnya, QGIS menyediakan cara yang lebih baik untuk menghitung jarak menggunakan geometri ellipsoidal, yang merupakan metode paling akurat untuk lapisan yang mencakup area yang luas seperti ini. Pilih Ellipsoidalsebagai opsi Hitung menggunakan . Klik Jalankan . Setelah proses selesai, klik Tutup.
5.	Anda akan melihat layer baru dimuat di panel Layers . Ini adalah salinan dari lapisan input dengan kolom baru yang ditambahkan untuk jarak. Klik kanan layer dan pilih Open Attribute Table .Added geom infoAdded geom info
6.	Di Tabel Atribut , Anda akan melihat kolom baru bernama distance . Ini berisi panjang setiap garis fitur dalam meter . Perhatikan juga atribut sov_a3 yang berisi kode negara untuk setiap fitur. Tutup jendela Tabel Atribut .
7.	Sekarang setelah kita memiliki panjang segmen jalur kereta api individual, kita dapat menjumlahkannya untuk menemukan panjang total rel kereta api. Tetapi karena pernyataan masalah menuntut kita membutuhkan total panjang rel kereta api di Amerika Serikat, kita harus menggunakan hanya segmen-segmen yang ada di AS. Kita dapat menggunakan nilai kode negara di kolom sov_a3 untuk memfilter layer. Klik kanan layer dan pilih Filter .Added geom info
8.	Dalam dialog Pembuat Kueri , masukkan ekspresi berikut dan klik OK ."sov_a3" = 'USA'
9.	Anda akan melihat ikon Filter muncul di sebelah layer di panel Layers yang menunjukkan bahwa filter diterapkan ke layer. Anda juga dapat mengonfirmasi secara visual bahwa lapisan sekarang berisi segmen garis hanya untuk Amerika Serikat. Sekarang kita siap untuk menghitung jumlahnya. Klik tombol Tampilkan ringkasan statistik di Bilah Alat Atribut .Added geom info
10.	Panel Statistik baru akan terbuka. Pilih lapisan dan kolom.Added geom infolength
11.	Anda akan melihat berbagai statistik ditampilkan di panel. Satuan statistik sama dengan satuan lengthkolom- meter . Mari ubah perhitungan untuk menggunakan kilometer sebagai gantinya. Klik ikon Ekspresi di sebelah menu tarik-turun bidang di panel Statistik .
12.	Masukkan ekspresi berikut dalam Dialog Ekspresi yang mengubah panjang menjadi kilometer.
length / 1000
13.	Nilai Jumlah yang ditampilkan adalah total panjang rel kereta api di AS.

# Basic Raster Styling and Analysis (QGIS3) (Project 6)
1.	Buka QGIS dan cari file yang diunduh di panel Browser . Perluas gpw-v4-population-count-rev11_2000_2pt5_min_tif.zipfile dan seret gpw-v4-population-count-rev11_2000_2pt5_min.tiffile ke kanvas.

2.	Layer baru gpw-v4-population-count-rev11_2000_2pt5_minakan ditambahkan ke panel Layers . Demikian pula, cari gpw-v4-population-count-rev11_2010_2pt5_min_tif.zipfile dan seret gpw-v4-population-count-rev11_2010_2pt5_min.tiffile ke kanvas.

3.	Mari jelajahi lapisan ini. Klik tombol Identifikasi pada Bilah Alat Atribut . Setelah alat dipilih, klik titik mana pun di kanvas.

4.	Nilai yang terkait dengan piksel itu akan ditampilkan di panel Identifikasi Hasil baru. Di panel Identifikasi Hasil , ubah Mode menjadi . Ini akan menampilkan nilai piksel dari semua raster, bukan hanya lapisan paling atas. Bandingkan nilai dari kedua lapisan. Karena resolusi raster kira-kira 5km x 5km, nilai piksel mewakili total populasi di area (25 km persegi) yang diwakili oleh piksel.Top down

5.	Tutup panel Identifikasi Hasil . Mari kita buat visualisasi layer yang lebih baik. Klik tombol Open the layer Styling panel di panel Layers .

6.	Di panel Layer Styling , klik dropdown Render type dan pilih renderer.Singleband pseudocolor

7.	Renderer ini akan memberi style pada layer menggunakan color ramp. Ramp warna default adalah putih-merah di mana nilai minimum akan diberi warna putih dan nilai maksimum di lapisan akan diberi warna merah. Nilai tengah akan diberi warna interpolasi linier merah. Perluas Pengaturan Nilai Min / Maks dan pilih opsi. Anda akan melihat bahwa visualisasi peta sekarang jauh lebih baik. Rentang data standar ditetapkan dari 2% hingga 98% dari nilai data, artinya outlier tidak akan digunakan untuk menetapkan nilai minimum dan maksimum, sehingga menghasilkan visualisasi yang jauh lebih representatif.Cumulative count cut

8.	Tutup panel Layer Styling . Kita bisa menerapkan gaya serupa ke lapisan lain juga. Namun ada cara yang lebih mudah untuk mentransfer gaya dari satu lapisan ke lapisan lainnya. Klik kanan gpw-v4-population-count-rev11_2010_2pt5_minlayer dan pilih Styles ‣ Copy Style .

9.	Sekarang klik kanan gpw-v4-population-count-rev11_2000_2pt5_minlayer un-style dan pilih Styles Paste Style .

10.	Parameter gaya yang sama akan diterapkan ke lapisan lainnya. Fitur ini sangat berguna ketika Anda ingin membandingkan lapisan yang berbeda menggunakan kategorisasi yang sama. Saat Anda mengaktifkan visibilitas lapisan atas, Anda dapat melihat perubahan populasi secara visual.

11.	Tugas kita adalah membuat peta tematik dari perubahan populasi. Mari hitung selisih antara 2 layer dan buat raster lain di mana setiap piksel mewakili perubahan dalam populasi. Pergi ke Raster ‣ Kalkulator raster .

12.	Di bagian Raster bands , Anda dapat memilih layer dengan mengklik dua kali pada layer tersebut. Band diberi nama setelah nama raster diikuti dengan @dan nomor band. Karena setiap raster kami hanya memiliki 1 band, Anda akan diberi nama dengan @1ditambahkan ke nama layer. Kalkulator raster dapat menerapkan operasi matematika pada piksel raster. Dalam hal ini kita ingin memasukkan rumus sederhana untuk mengurangkan populasi tahun 2010 dari tahun 2000. Masukkan ekspresi berikut. Selanjutnya, klik tombol … di sebelah Output layer .

"gpw-v4-population-count-rev11_2010_2pt5_min@1" - "gpw-v4-population-count-rev11_2000_2pt5_min@1"
13.	Masukkan population_change_2010_2000.tifsebagai file Output . Klik OK untuk memulai perhitungan.
14.	Setelah selesai, layer baru population_change_2010_2000akan ditambahkan ke panel Layers . Mari ubah gaya sehingga perubahan populasi negatif dan positif divisualisasikan dengan lebih baik. Klik tombol Open the layer Styling panel di panel Layers .
15.	Salah satu pilihannya adalah menggunakan teknik penataan yang sama seperti sebelumnya dan memilih jalur warna yang berbeda. Klik drop-down Color ramp dan pilih Spectralramp. Klik tarik-turun lagi dan pilih untuk menetapkan warna biru ke nilai rendah dan merah ke nilai tinggi.Invert Color Ramp
16.	Ini adalah visualisasi yang bagus, tetapi tidak mudah untuk ditafsirkan. Mari buat peta yang lebih baik dengan 4 kategori terpisah, Decline, Neutral, Growthdan . Gulir ke bawah ke tabel dengan kelas. Tahan tombol dan pilih semua baris. Klik tombol Hapus baris yang dipilih .High GrowthShift
17.	Ubah mode InterpolasiDiscrete ke . Sekarang kita akan membuat peta warna secara manual. Klik tombol Tambahkan nilai secara manual . Masukkan -100sebagai Nilai dan Declinesebagai Label . Tetapkan warna biru untuk kategori ini. Cara kerja peta warna adalah semua nilai yang lebih rendah dari nilai yang dimasukkan akan diberi warna entri tersebut. Anda akan melihat kanvas hanya akan menampilkan area dengan perubahan populasi negatif.
18.	Lengkapi peta warna dengan nilai yang sesuai. Saya memilih 100, 1000dan 100000sebagai batas atas untuk Neutral, Growthdan kategori masing-masing. Tetapkan warna untuk setiap kategori yang dibuat, misalnya krem, oranye, dan merah.High Growth
19.	Setelah Anda puas dengan visualisasi, tutup panel Layer Styling . Anda sekarang memiliki peta tematik global tentang perubahan populasi.

# Raster Mosaicing and Clipping (QGIS3)
1.	Buka QGIS dan temukan file yang diunduh di panel Browser . Perluas file zip individual untuk menampilkan .hgtfile. Tahan Ctrltombol dan pilih semua file individual. Setelah dipilih, seret ke kanvas.
2.	Anda akan melihat 11 lapisan individu dimuat di panel Lapisan dan ditampilkan di kanvas. Kami akan menggabungkan ubin individu ini menjadi satu mosaik. Pergi ke Memproses ‣ Kotak Alat .
3.	Cari dan temukan GDAL Raster miscellaneous Merge tool. Klik dua kali untuk meluncurkannya.
4.	Dalam dialog Gabung , klik tombol … di sebelah Lapisan masukan . Klik Select All untuk memilih semua layer individual.
5.	Seperti disebutkan dalam rincian lapisan dataset , tipe data masukan adalah bilangan bulat bertanda 16-bit . Untuk menjaga integritas data, kita harus menyimpan tipe data yang sama untuk layer gabungan. Pilih Int16sebagai tipe data Keluaran . Juga format data keluaran default adalah GeoTiff. File GeoTiff bisa menjadi sangat besar jika tidak dikompresi. Pilih sebagai Profil . Klik Jalankan .High Compression
6.	Setelah pemrosesan selesai, layer baru OUTPUTakan ditambahkan ke panel Layers . Jika lapisan tidak berada di bagian atas tumpukan, pilih dan seret ke bagian atas panel Lapisan .
7.	Anda akan melihat bahwa OUTPUTlapisan berisi data elevasi gabungan dari ubin masukan individual. Visualisasi default hanya menampilkan nilai piksel dalam kisaran 0-255. Namun data kami berisi piksel dengan nilai -14 hingga 2371, menghasilkan rendering kontras yang rendah. Mari kita ubah menjadi visualisasi yang lebih baik. Klik tombol Open the layer Styling panel di panel Layers .
8.	Di panel Layer Styling , klik dropdown Render type dan pilih Hillshaderenderer. Opsi rendering ini sangat cocok untuk data elevasi.
9.	Operasi umum lainnya saat bekerja dengan raster adalah dengan memotong raster ke area yang Anda minati. Untuk tutorial ini, kami akan mengklip layer gabungan ke batas negara untuk Sri Lanka. Temukan ne_10m_admin_0_countries.zipfile yang diunduh dan perluas. Seret ne_10m_admin_0_countries.shpfile ke kanvas.
10.	ne_10m_admin_0_countriesPilih layer yang baru ditambahkan di panel Layers . Klik tombol Select Features by area atau single click pada Attributes Toolbar . Setelah dipilih, klik poligon Sri Lanka untuk memilihnya.
11.	Tetap pilih apa adanya dan buka Processing ‣ Toolbox . Cari dan temukan GDAL ‣ Ekstraksi raster ‣ Klip raster dengan alat lapisan topeng. Klik dua kali untuk meluncurkannya.
12.	Dalam dialog Clip Raster by Mask Layer , tetapkan OUTPUTsebagai Input Layer . Pilih ne_10m_admin_0_countriessebagai layer Mask , dan centang kotak Selected features only . Masukkan 0.0000sebagai Menetapkan nilai nodata yang ditentukan ke band keluaran . Seperti sebelumnya, pilih sebagai Profile . Klik Jalankan .High compression
13.	Layer baru OUTPUTakan ditambahkan ke panel Layers . Pada titik ini, mungkin sulit untuk melihat hasilnya karena kita memiliki terlalu banyak lapisan tumpang tindih yang terlihat. Klik tombol Kelola Tema Peta di panel Lapisan dan pilih .Hide All Layers
14.	Nyalakan hanya OUTPUTlayer terbaru dan beri gaya dengan Hilshadeperender seperti yang dilakukan sebelumnya.
15.	Lapisan elevasi keluaran gabungan dan subset untuk Sri Lanka sudah siap.

# Working with Terrain Data (QGIS3)
1.	Buka Lapisan ‣ Tambahkan Lapisan ‣ Tambahkan Lapisan Raster .
2.	Klik pada … di bawah Source , cari dan pilih file bernama 10n060e_20101117_gmted_mea300.tif .
3.	Anda akan melihat data medan yang ditampilkan di Kanvas QGIS. Setiap piksel dalam raster medan mewakili ketinggian rata-rata dalam meter di lokasi tersebut. Piksel gelap mewakili area dengan ketinggian rendah dan piksel yang lebih terang mewakili area dengan ketinggian tinggi.
4.	Mari temukan bidang minat kita. Dari Wikipedia , kami menemukan bahwa koordinat untuk area yang kami minati - Gunung Everest - terletak di koordinat 27.9881° N, 86.9253° E. Perhatikan bahwa QGIS menggunakan koordinat dalam format (X, Y), jadi Anda harus menggunakan koordinat sebagai (Bujur, Lintang). Rekatkan 86.9253,27.9881 ini di bagian bawah jendela QGIS yang bertuliskan Koordinasi dan tekan Enter`. Area pandang akan dipusatkan pada koordinat ini. Untuk memperbesar, Masukkan 1:1000000 di bidang Skala dan tekan Enter. Anda akan melihat viewport memperbesar area sekitar Himalaya.
5.	Kami sekarang akan memotong raster ke area yang diminati ini. Cari Klip di Processing Toolbox . Pilih di bawah algoritma GDAL.Clip Raster by extent
6.	Di jendela Clip Raster by Extent , pilih 10n060e_20101117_gmted_mea300sebagai Input Layer , klik ...di Clipping extent dan pilih , klik di Clipped (extent) dan masukkan namanya sebagai . Klik Jalankan .Use Map canvas extent...mt_everest.tif
7.	Sebuah layer baru mt_everestakan muncul di kanvas. Cari Hill di Processing Toolbox . Pilih Hillshadealgoritma di bawah algoritma GDAL.
8.	Di jendela Hillshade , pilih mt_everestsebagai Elevation Layer , masukkan Azimuth (horizontal angle)315.000 , masukkan Vertical angle . Klik di Hillshade dan masukkan nama sebagai . Klik Jalankan .45.000...mt_everest_hillshade.tif
9.	Sebuah layer baru mt_everest_hillshadeakan muncul di kanvas.
10.	Cari Kontur di Processing Toolbox . Pilih Contouralgoritma di bawah algoritma GDAL.
11.	Di jendela Contour , pilih mt_everestsebagai Input Layer , masukkan Interval 250antara garis kontur . Klik ...di Contours dan masukkan namanya sebagai mt_everest_contour.gpkg. Klik Jalankan .
12.	Sebuah layer baru mt_everest_contourakan muncul di kanvas. Klik kanan pada layer dan klik Open Attribute Table .
13.	Anda akan melihat bahwa setiap fitur baris memiliki atribut bernama ELEV . Ini adalah ketinggian dalam meter yang diwakili oleh setiap garis. Klik pada tajuk kolom beberapa kali untuk mengurutkan nilai dalam urutan menurun. Di sini Anda akan menemukan garis yang mewakili elevasi tertinggi dalam data kami, yaitu Gunung Everest.
14.	Pilih baris atas, dan klik tombol Zoom to selection .

15.	Beralih ke jendela QGIS utama. Anda akan melihat garis kontur yang dipilih disorot dengan warna kuning. Ini adalah area elevasi tertinggi dalam dataset kami.
16.	Cari Smooth di Processing Toolbox . Pilih di Smoothbawah Geometri vektor.
17.	Di jendela Smooth , pilih mt_everest_contoursebagai Input Layer , masukkan 5di Iterations . Klik Jalankan .
18.	Sebuah layer baru Smoothedakan muncul di kanvas. Lapisan ini akan memiliki tepi yang lebih halus dibandingkan dengan mt_everest_contourlapisan.
19.	Anda juga dapat memvisualisasikan lapisan kontur dan memverifikasi analisis Anda dengan mengekspor lapisan kontur sebagai KML dan melihatnya di Google Earth. Klik kanan pada layer yang telah dihaluskan, pilih Export Save Feature As… .
20.	Pilih Keyhole Markup Language [KML] sebagai Format . Klik ...di Nama file dan masukkan nama sebagai contour_smoothed.kml. Klik Oke .
21.	Jelajahi file keluaran di disk Anda dan klik dua kali untuk membuka Google Earth Pro.

# Working with WMS Data (QGIS3)
1.	Buka QGIS dan klik Buka Pengelola Sumber Data .
2.	Di kotak dialog Pengelola Sumber Data alihkan ke WMS/WMTS , klik Baru .
3.	Di kotak dialog Buat Koneksi WMS/WMTS Baru di bawah Detail Koneksi , masukkan Nama sebagai SEDAC, dan tempel URL yang disalin di kotak teks URL . Klik Oke . Jika Anda mendapatkan kesalahan dengan URL yang disalin, coba dengan URL alternatif https://sedac.ciesin.columbia.edu/geoserver/ows.
4.	Sekarang di kotak dialog Pengelola Sumber Data , klik Sambungkan . Semua lapisan yang tersedia akan dimuat. Anda akan melihat ID berbeda yang tercantum di sebelah lapisan. ID 0berarti Anda mendapatkan peta dari semua lapisan. Jika Anda tidak menginginkan semua lapisan, Anda dapat memperluas daftar dengan mengeklik ikon ▸ dan memilih lapisan yang diinginkan.
5.	Untuk tutorial ini, kami tertarik pada lapisan tertentu. Telusuri . Pilih versi default dari lapisan perluasan kota 2030.Probabilities of Urban Expansion to 2030

6.	Di bagian Pengkodean Gambar , Anda harus memilih format gambar. Format gambar itu penting, dan tergantung pada kasus penggunaan. Berdasarkan perspektif pengguna, berikut adalah beberapa petunjuk,
7.	Kualitas : Kompresi file untuk PNG adalah lossless, untuk JPEG itu adalah kompresi lossy dan TIFF dapat berupa keduanya. Itu berarti kualitas PNG akan lebih baik dibandingkan dengan JPEG. Jika tujuan utama Anda adalah mencetak peta, gunakan PNG.
8.	Kecepatan : Karena gambar PNG tidak terkompresi dan dengan demikian ukurannya lebih besar, mereka akan membutuhkan waktu lebih lama untuk dimuat. Jika Anda menggunakan lapisan dalam proyek Anda sebagai lapisan referensi dan perlu banyak memperbesar/menggeser, gunakan JPEG.
9.	Dukungan Klien : QGIS mendukung sebagian besar format, tetapi jika Anda sedang mengembangkan aplikasi web, browser biasanya tidak mendukung TIFF, jadi Anda harus memilih format lain.
10.	Jenis data : Jika lapisan Anda terutama vektor, PNG akan memberikan hasil yang lebih baik. Untuk lapisan citra, JPEG biasanya merupakan pilihan yang lebih baik.
11.	Untuk tutorial ini, pilih PNG sebagai formatnya. Ubah nama Layer jika Anda mau dan klik Add .
12.	Sekarang lapisan Probabilitas Ekspansi Perkotaan hingga 2030 akan dimuat di kanvas. Gunakan alat Zoom/Pan untuk menjelajahi lapisan. Cara kerja layanan WMS adalah setiap kali Anda memperbesar/menggeser, ia mengirimkan koordinat area pandang Anda ke server dan server membuat gambar untuk area pandang tersebut dan mengembalikannya ke klien. Jadi, akan ada beberapa penundaan sebelum Anda melihat gambar untuk area tersebut setelah Anda memperbesar. Oleh karena itu, koneksi internet selalu diperlukan untuk mengakses lapisan ini.
13.	Sekarang, perbesar ke tempat yang diketahui dan klik ikon Identifikasi Fitur di bilah alat.
14.	Klik pada piksel apa saja di kanvas, itu akan memunculkan kotak dialog dengan nilai sel. Ini adalah nilai piksel dalam lapisan - yang mewakili kemungkinan bahwa piksel tersebut akan mengalami urbanisasi pada tahun 2030. Karena lapisan tersebut tidak disimpan secara lokal, nilai ini diambil dari penyedia layanan. Anda dapat melihat hasilnya lebih baik dengan memilih Format as HTMLdan View as Tree.
15.	Untuk melihat, informasi tambahan tentang layer klik kanan pada layer dan pilih Properties… .
16.	Di kotak dialog Properti Lapisan , alihkan ke tab Informasi di sini semua informasi seperti penyedia data , proyeksi , jangkauan dapat ditemukan. Klik OK untuk menutup kotak dialog setelah menjelajah.
17.	Di QGIS Browser , cari XYZ Tiles dan klik dan seret OpenStreetMapke kanvas.
18.	Klik pada ikon panel Open the Layer Styling dan alihkan ke Transparency .
19.	Atur opacity Global ke50 %
20.	Sekarang di kanvas, lapisan Urban dapat dieksplorasi dengan referensi geografis.
21.	Untuk mendapatkan lebih banyak akses ke transparansi layer, klik kanan pada layer dan pilih Properties… .
22.	Di kotak dialog Properti Lapisan , alihkan ke tab Legenda , di bawah Widget yang tersedia pilih dan klik Tambahkan ikon widget yang dipilih. Klik Oke .Opacity slider
23.	Sekarang widget penggeser akan tersedia untuk mengontrol opacity layer.

# Working with Projections (QGIS3)
1.	Buka QGIS. Pergi ke Layer Add Layer Add Vector Layer… .
2.	Klik … di sebelah Sumber , Jelajahi ne_10m_admin_0_countries.shpfile yang diunduh dan klik Tambah .
3.	Di bagian bawah jendela QGIS, Anda akan melihat label Coordinate . Saat Anda menggerakkan kursor di atas peta, koordinat X dan Y di lokasi tersebut akan ditampilkan. Di pojok kanan bawah Anda akan melihat EPSG:4326 . Ini adalah kode untuk CRS (Projection) saat ini untuk proyek - juga dikenal sebagai Project CRS .
4.	Untuk menentukan proyeksi layer, kita dapat melihat ke dalam metadata. Klik kanan pada ne_10m_admin_0_countrieslayer dan pilih Properties .
5.	Beralih ke tab Informasi dalam dialog Properti Lapisan . Perluas bagian Informasi dari penyedia . Di bagian bawah, Anda akan melihat nama proyeksi di bawah CRS .
6.	Sekarang mari kita lihat bagaimana kita bisa mengubah proyeksi layer. Operasi ini disebut Re-Projection . Daripada memproyeksikan ulang seluruh lapisan, kita juga dapat memilih subset fitur dan memproyeksikannya kembali ke lapisan baru. Gunakan alat Select features by area or single click dan klik fitur United Kingdom untuk memilihnya.
7.	Cari dan temukan algoritma Vector General ‣ Proyeksi ulang layer di kotak alat Pemrosesan.

8.	Pilih ne_10m_admin_0_countriessebagai lapisan Input , centang Selected features only lalu klik ikon globe di sebelah Target CRS , cari dan pilih . Di Reprojected , pilih dan klik Save to a file . Sekarang pilih direktori dan masukkan nama as dan klik Run .EPSG:27700 - OSGB 1936 / British National Grid...united_kingdom.gkpg

9.	Sebuah layer baru united_kingdomakan muncul di Layer Panel . Seperti yang Anda lihat, kedua lapisan masih sejajar satu sama lain - meskipun mereka berada di CRS yang berbeda. Ini karena QGIS mendukung transformasi CRS On-The-Fly (OTF) . Artinya, setiap kali CRS lapisan tidak cocok dengan CRS Proyek, maka secara otomatis akan diubah menjadi CRS Proyek sehingga dapat ditampilkan dengan benar. Sekarang mari kita atur Project CRS agar sesuai dengan CRS united_kingdomLayer yang baru dibuat. Hapus ne_10m_admin_0_countrieslayer dan, klik kanan pada united_kingdomlayer Layer CRS Set Project CRS dari Layer .

10.	Anda akan melihat Project CRS diperbarui ke EPSG:27700.

11.	Sekarang mari kita tambahkan layer Raster. Pergi ke Layer Add Layer Add Raster Layer… .

12.	Klik di ...sebelah Source , pilih layer MiniScale_(standard)_R23.tif. Klik Tambahkan .

13.	Sekarang layer baru MiniScale_(standard)_R23ditambahkan ke kanvas.

14.	Untuk membuat kedua lapisan terlihat, alihkan urutan lapisan dengan menyeret MiniScale_(standard)_R23ke bawah di panel Lapisan .

15.	Klik kanan pada MiniScale_(standard)_R23layer dan klik Properties .

16.	Di Layer Properties , pindah ke Information , CRS adalah . Ini menegaskan bahwa CRS layer raster sama dengan Project CRS.EPSG:27700 - OSBG 1935 / British National Grid - Projected

# Georeferencing Topo Sheets and Scanned Maps (QGIS3)
1.	Buka QGIS dan klik Raster ‣ Georeferencer untuk membuka alat.
2.	Dari QGIS versi 3.26 dan seterusnya, Georeferencer dapat diluncurkan dari Layer ‣ Georeferencer .
3.	Georeferensi dibagi menjadi 2 bagian. Bagian atas tempat gambar akan ditampilkan dan bagian bawah tempat tabel yang menunjukkan GCP Anda akan muncul.
4.	Sekarang kita akan membuka gambar JPG kita. Buka File Buka Raster . Jelajahi gambar yang diunduh dari peta yang dipindai dan klik Buka .
5.	Anda akan melihat gambar akan dimuat di bagian atas. Anda dapat menggunakan kontrol zoom/pan pada bilah alat untuk mempelajari lebih lanjut tentang peta.
6.	Sekarang kita perlu menetapkan koordinat ke beberapa titik di peta ini. Jika Anda melihat lebih dekat, Anda akan melihat kotak koordinat dengan tanda. Ini adalah garis grid Lintang dan Bujur.
7.	Sebelum menambahkan Ground Control Points (GCP), kita perlu mendefinisikan Pengaturan Transformasi. Klik ikon roda gigi di jendela georeferensi untuk membuka dialog pengaturan Transformasi.
8.	Dalam dialog Pengaturan transformasi , pilih jenis Transformasi sebagai . Lihat Dokumentasi QGIS untuk mempelajari tentang berbagai jenis transformasi dan penggunaannya. Kemudian pilih metode Resampling sebagai . Klik tombol Select CRS di sebelah Target SRS .Polynomial 2Nearest neighbor
9.	Jika Anda melakukan geo-referensi peta yang dipindai seperti ini, Anda dapat memperoleh informasi CRS dari peta itu sendiri. Melihat gambar peta kita, koordinatnya ada di Lintang/Bujur. Tidak ada informasi datum yang diberikan, jadi kita harus mengasumsikan yang sesuai. Karena ini adalah India dan petanya cukup tua, kita bisa bertaruh bahwa data Everest 1830 akan memberi kita hasil yang baik. Cari everestdan pilih CRS dengan definisi terlama dari datum Everest (EPSG:4042). Klik Oke .
10.	Beri nama raster keluaran Anda sebagai 1870_southern_india_modified.tif. Pilih LZWsebagai Kompresi . Periksa Simpan poin GCP untuk menyimpan poin sebagai file terpisah untuk tujuan di masa mendatang. Pastikan opsi Muat di QGIS saat selesai dicentang. Klik Oke .
11.	Sekarang kita dapat mulai menambahkan Ground Control Points (GCP). Klik tombol Tambah Poin .
12.	Sekarang tempatkan cross-hair di persimpangan garis grid dan klik kiri, ini akan berfungsi sebagai ground-truth dalam kasus kita. Saat garis kisi diberi label, kita dapat menentukan koordinat X dan Y dari titik-titik dengan menggunakannya. Di jendela pop-up, masukkan koordinat. Ingat bahwa X=bujur dan Y=lintang. Klik Oke .
13.	Anda akan melihat tabel GCP sekarang memiliki baris dengan detail GCP pertama Anda.
14.	Demikian pula, tambahkan lebih banyak GCP yang mencakup seluruh gambar. Semakin banyak poin yang Anda miliki, semakin akurat gambar Anda terdaftar ke koordinat target. Transformasi membutuhkan setidaknya 6 GCP. Setelah Anda menambahkan jumlah minimum poin yang diperlukan untuk transformasi, Anda akan melihat bahwa GCP sekarang memiliki nilai kesalahan dan bukan nol . Jika GCP tertentu memiliki nilai kesalahan yang sangat tinggi, itu biasanya berarti kesalahan manusia dalam memasukkan nilai koordinat. Jadi, Anda dapat menghapus GCP tersebut dan merekamnya kembali. Anda juga dapat mengedit nilai koordinat di Tabel GCP dengan mengklik sel di salah satu Tujuan. X atau Tujuan. kolom Y.Polynomial 2dXdYResidual
15.	Setelah Anda puas dengan GCP, klik tombol Mulai Georeferensi . Ini akan memulai proses membengkokkan gambar menggunakan GCP dan membuat raster target.
16.	Setelah proses selesai, Anda akan melihat lapisan georeferensi dimuat di QGIS. Georeferensi sekarang selesai. Juga, Anda akan melihat Project CRS di kanan bawah diatur ke EPSG:4042 seperti yang dijelaskan di Pengaturan Transformasi.
17.	Seret dan lepas OpenStreetMapas Base Map dari dropdown XYZ Tiles di bagian bawah panel Browser untuk memverifikasi lapisan georeferensi. Untuk menyetel transparansi, klik ikon Open layer styling panel dan pilih tab Transparency . Atur transparansi menjadi . Sekarang gambar georeferensi harus dilapisi dengan garis peta dasar.40 %
18.	Jika georeferensi membutuhkan lebih banyak penyesuaian, kita dapat mulai dari poin GCP yang dikumpulkan. Telusuri 1870_southern_india_modified.tiflokasi file. Anda dapat menemukan file tambahan, 1870_southern_india_modified.tif.points. File ini akan berisi informasi poin GCP.
19.	Buka alat georeferensi di QGIS, klik File ‣ Load GCP Points , dan pilih 1870_southern_india_modified.tif.points. Ini akan memuat GCP yang dibuat sebelumnya. Kemudian muat 1870_southern_india_modified.tifuntuk menyempurnakan pekerjaan Anda.

# Georeferencing Aerial Imagery (QGIS3)
1.	Kami akan menggunakan peta dasar dari OpenStreetMap untuk menangkap koordinat georeferensi. QGIS3 hadir dengan dukungan built-in untuk lapisan petak. Ini umumnya dikenal sebagai lapisan 'XYZ' karena dibuat menggunakan petak peta individual untuk setiap tingkat zoom (z) pada petak koordinat ax,y. Anda dapat menemukan OpenStreetMaplapisan di bawah Ubin XYZ di Panel Peramban . Seret layer ke kanvas utama. Setelah dimuat, catat Sistem Referensi Koordinat (CRS) untuk lapisan ini di corder kanan bawah. Ini diatur sebagai . Ini penting karena koordinat yang kita simpulkan dari lapisan ini selama georeferensi akan berada di CRS ini.EPSG 3857 Pseudo Mercator
2.	Gambar yang kami georeferensi adalah untuk . Anda dapat memperbesar/menggeser untuk menemukan taman ini di peta. Tapi itu rumit dan tidak praktis. Dari QGIS versi 3.20 dan seterusnya, ada dukungan bawaan untuk Nominatim Geocoder berbasis OpenStreetMap. Klik bilah pencarian di kiri bawah jendela QGIS. Untuk menggunakan ini sebagai awalan geocoder, tempat pencarian dengan . Pencarian akan memunculkan daftar alamat yang dapat dipilih. Klik alamat pertama.Washington Square Park, New York>> Washington Square Park
3.	Kanvas peta akan dipusatkan ke Square Park. Sekarang mari kita mulai georeferensi. Luncurkan Georeferencer dari Raster Georeferencer .
4.	Untuk georeferensi gambar udara, kita harus memilih titik koordinat dari OpenStreetMap, jadi pertama-tama mari kita masukkan alat Georeferencer ke jendela utama QGIS. Pilih Konfigurasi Georeferensi dari Pengaturan Konfigurasikan Georeferensi .
5.	Centang Show georeferencer window docked dan klik OK .Jendela Georeferencer akan ditempatkan di bagian bawah jendela utama QGIS. Mari kita memuat file gambar dengan mengklik ikon Open Raster di jendela Georeferencer dan menavigasi ke file JPG yang diunduh. Klik Buka.
6.	Sebelum menambahkan Titik Kontrol Tanah (GCP), kita perlu menentukan Pengaturan Transformasi. Klik ikon Pengaturan Transformasi untuk membuka dialog Pengaturan Transformasi. Pilih jenis Transformasi sebagai . Lihat Dokumentasi QGIS untuk mempelajari tentang berbagai jenis transformasi dan penggunaannya. Seperti disebutkan sebelumnya, peta dasar kita ada di CRS, jadi tetapkan itu sebagai Target CRS . Anda dapat membiarkan nama raster Output ke default dan memilih sebagai Compression . Periksa Gunakan 0 untuk transparansi bila diperlukan . Periksa Simpan poin GCPPolynomial 2EPSG 3857 Pseudo MercatorLZWuntuk menyimpan poin sebagai file terpisah untuk tujuan masa depan. Pastikan opsi Muat di QGIS saat selesai dicentang. Klik Oke .
7.	Sekarang klik tombol Add Point pada toolbar dan pilih lokasi yang mudah dikenali pada gambar. Sudut, persimpangan, tiang dll, membuat titik kontrol yang baik. Setelah Anda mengklik gambar di lokasi titik kontrol, Anda akan melihat pop-up yang meminta Anda untuk memasukkan koordinat peta. Klik tombol Dari kanvas peta .
8.	Di OpenStreetMaplapisan, klik pada lokasi yang tepat di lapisan referensi. Koordinat akan terisi otomatis dari klik Anda pada kanvas peta. Klik Oke .
9.	Demikian pula, pilih setidaknya 6 titik pada gambar dan tambahkan koordinatnya dari lapisan referensi. Setelah Anda menambahkan jumlah minimum poin yang diperlukan untuk transformasi, Anda akan melihat bahwa GCP sekarang memiliki nilai bukan nol dX, dY, dan Residualkesalahan. Jika GCP tertentu memiliki nilai kesalahan yang sangat tinggi, itu biasanya berarti kesalahan manusia dalam memasukkan nilai koordinat. Jadi, Anda dapat menghapus GCP itu dan menangkapnya lagi.
10.	Setelah Anda puas dengan GCP, klik Mulai georeferensi . Ini akan memulai proses membengkokkan gambar menggunakan GCP dan membuat raster target. Setelah proses selesai, Anda akan melihat layer dimuat di QGIS. Tutup jendela Georeferensi .
11.	Sekarang klik pada ikon panel penataan lapisan Terbuka dan Beralih ke tab Transparansi . Tambahkan 255sebagai nilai tambahan tanpa data . Ini akan menghapus batas putih di sekitar gambar. Sekarang Anda akan melihat gambar georeferensi Anda terhampar dengan baik di lapisan dasar.

# Digitizing Map Data (QGIS3)
1.	Di QGIS, mari kita memuat file gambar. Pergi ke Layer Add Layer Add Raster Layer .
2.	Dalam dialog Pengelola Sumber Data pilih Raster. Di bawah Sumber klik ...dan cari yang diunduh BX24_GeoTifv1-02.tifdan klik Buka . Kemudian klik Tambah diikuti dengan Tutup.
3.	Ini adalah file raster yang besar, dan Anda mungkin memperhatikan bahwa saat Anda memperbesar atau menggeser peta, peta memerlukan sedikit waktu untuk merender gambar. QGIS menawarkan solusi sederhana untuk membuat raster memuat lebih cepat dengan menggunakan Image Pyramids . QGIS membuat petak pra-render pada resolusi yang berbeda, dan ini disajikan kepada Anda alih-alih raster penuh. Ini membuat navigasi peta cepat dan responsif. Klik kanan BX24_GeoTifv1-02layer dan pilih Properties .
4.	Dalam dialog Properti Lapisan , Pilih tab Piramida . Tahan Ctrltombol dan pilih semua resolusi yang ditawarkan di panel Resolusi . Biarkan opsi lain ke default dan klik Bangun piramida .
5.	Setelah proses selesai, kotak dialog akan menampilkan piramida tanpa tanda silang. Ini menandakan pembangunan Piramida Gambar sudah selesai. Klik Oke .
6.	Sebelum kita mulai, kita perlu mengatur Opsi Digitizing default . Buka Pengaturan Opsi… .
7.	Pilih tab Digitizing dalam dialog Opsi . Periksa Aktifkan gertakan secara default di bawah bagian Snapping . Dalam mode jepret default pilih Vertex . Ini akan memungkinkan Anda untuk snap ke vertex terdekat. Saya juga lebih memilih untuk mengatur toleransi gertakan default dan radius Pencarian untuk suntingan titik dalam piksel daripada unit peta. Ini akan memastikan bahwa jarak gertakan tetap konstan terlepas dari tingkat zoom. Tergantung pada resolusi layar komputer Anda, Anda dapat memilih nilai yang sesuai. Klik Oke .
8.	Sekarang kita siap untuk memulai digitalisasi. Pertama-tama kita akan membuat layer jalan dan mendigitalkan jalan di sekitar area taman. Klik Layer ‣ Create Layer ‣ New GeoPackage Layer… ikon dari Panel. GeoPackage adalah format data terbuka, non-proprietary, platform-independen, dan berbasis standar untuk sistem informasi geografis yang diimplementasikan sebagai wadah database SQLite. Ini membuatnya lebih mudah untuk memindahkannya daripada sekumpulan shapefile. Dalam tutorial ini, kami membuat beberapa lapisan poligon dan lapisan garis sehingga GeoPackage akan lebih cocok. Anda selalu dapat memuat GeoPackage dan mengekspor layer sebagai shapefile atau format lain yang Anda inginkan.
9.	Dalam dialog Lapisan GeoPackage Baru , klik tombol … dan simpan database GeoPackage baru bernama digitizing.gpkg. Pilih nama Tabel sebagai Roadsdan pilih LineStringsebagai jenis Geometri . Peta topografi dasar adalah CRS.EPSG:2193 - NZGD 2000
10.	Saat membuat lapisan GIS, Anda harus memutuskan atribut setiap fitur. Karena ini adalah layer jalan, kita juga akan memiliki dua atribut utama - Nama dan Kelas. Di Bidang Baru Masukkan Namejenis data Teks, dengan panjang Maksimum50 dan klik Tambahkan ke daftar atribut. Sekarang buat atribut baru dengan tipe Text data , dengan sebagai Maximum length . Klik OkeClass50
11.	Setelah Roadslapisan dimuat, klik tombol Toggle Editing untuk menempatkan lapisan dalam mode pengeditan.
12.	Klik tombol Tambahkan Fitur Garis . Klik pada kanvas peta untuk menambahkan simpul baru. Tambahkan simpul baru bersama dengan fitur jalan. Setelah Anda mendigitalkan ruas jalan, klik kanan untuk mengakhiri fitur.
13.	Setelah Anda mengklik kanan untuk mengakhiri fitur, Anda akan mendapatkan dialog pop-up bernama Road - Feature Attributes . Di sini Anda dapat memasukkan atribut dari fitur yang baru dibuat. Lewati memasukkan nilai apa pun untuk fid karena ini adalah id berurutan yang akan dibuat secara otomatis. Masukkan nama jalan seperti yang muncul di peta topo. Secara opsional, tetapkan nilai Kelas Jalan juga. Klik Oke .
14.	Gaya default dari layer garis baru adalah garis tipis. Mari kita ubah untuk lebih melihat fitur digital di kanvas. Pilih Roadslayer dan klik Layer Styling Panel .
15.	Di Layer Styling Panel , cari gaya layer jalan yang berbeda. Pilih . Klik Oke .topo road
16.	Sekarang lapisan jalan akan terlihat jelas. Jika Anda puas dengan pekerjaannya, klik tombol Save Layer Edits untuk menyimpan perubahan.
17.	Sebelum kita mendigitalkan jalan yang tersisa, penting untuk memperbarui beberapa pengaturan snap penting lainnya untuk membuat lapisan bebas kesalahan. Klik kanan pada ruang mana pun di area bilah alat dan aktifkan bilah alat Snapping.
18.	Sekarang Enable Snapping (Magnet Icon) akan muncul di panel. Klik untuk mengaktifkannya dan pilih All Layers dan pilih .Open Snapping Options..
19.	Dalam dialog Snapping options , klik Snapping on Intersection , yang memungkinkan Anda menjepret perpotongan lapisan latar belakang.
20.	Sekarang Anda dapat mengklik tombol Tambahkan fitur dan mendigitalkan jalan lain di sekitar taman. Pastikan untuk mengklik Simpan Hasil Editan setelah menambahkan fitur baru untuk menyimpan pekerjaan Anda. Alat yang berguna untuk membantu Anda mendigitalkan adalah Alat Vertex . Klik tombol Alat Vertex dan pilih .Vertex Tool (Current Layer)
21.	Setelah alat simpul diaktifkan, klik fitur apa saja untuk menampilkan simpul. Klik pada sembarang titik untuk memilihnya. Titik akan berubah warna setelah dipilih. Sekarang Anda dapat mengklik dan menyeret mouse Anda untuk memindahkan vertex. Ini berguna ketika Anda ingin melakukan penyesuaian setelah fitur dibuat. Anda juga dapat menghapus simpul yang dipilih dengan mengklik Deletetombol. ( di mac)Option+Delete
22.	Setelah Anda selesai mendigitalkan semua jalan, klik tombol Toggle Editing . Klik Simpan .
23.	Sekarang kita akan membuat layer lain untuk mendigitalkan taman sebagai poligon. Klik Layer Create Layer New GeoPackage Layer… icon dari Panels. Pada dialog New GeoPackage Layer , klik tombol … dan pilih database GeoPackage bernama digitizing.gpkg. Beri nama layer baru sebagai atribut yang disebut Parks. Pilih MultiPolygonsebagai Jenis . Peta topografi dasar adalah CRS. Klik Oke . Di Bidang Baru Masukkan , dan ketik sebagai Data teks , dengan Panjang maksimum dan klik :guilabel:` Tambahkan ke Daftar Bidang.`. Klik Oke .EPSG:2193 - NZGD 2000Name50
24.	Multi-Polygon - Digunakan untuk mewakili area dengan lubang di dalam atau terdiri dari beberapa area yang terputus-putus. Misalnya, 3 poligon diskontinyu dapat digambar dan dikelompokkan sebagai fitur tunggal.
25.	Dialog pop-up akan muncul. Pilih tombol Tambahkan Lapisan Baru .

26.	Sekarang pilih layer Parkslalu klikroad Toggle Editing dan klik tombol Add feature dan klik pada kanvas peta untuk menambahkan simpul poligon. Digitalkan poligon yang mewakili taman. Pastikan Anda menjepret simpul jalan sehingga tidak ada celah antara poligon taman dan garis jalan. Klik kanan untuk menyelesaikan poligon.

27.	Masukkan nama taman di pop-up Taman - Atribut Fitur .

28.	Sekarang mendigitalkan wilayah atas taman. Masukkan nama taman dan simpan perubahannya.

29.	Sekarang, sebelum mendigitalkan poligon dalam, mari atur pengaturan yang dapat memudahkan pekerjaan ini. Lapisan Multi-Poligon menawarkan pengaturan berguna lainnya yang disebut Hindari persimpangan poligon baru . Pilih Enable Snapping (Magnet Icon), klik untuk mengaktifkannya, dan klik All Layers dan pilih .Advanced Configuration

30.	Klik tombol di bilah alat gertakan.Avoid Overlap on Active layers

31.	Sekarang di Edit Konfigurasi Lanjutan , pilih Unit sebagai pixels.

32.	Centang kotak di kolom Hindari Tumpang tindih di baris untuk Parkslapisan.

33.	Klik Tambahkan fitur untuk menambahkan poligon. Dengan Avoid Overlap , Anda akan dapat dengan cepat mendigitalkan poligon baru tanpa khawatir akan menjepret tepat ke poligon tetangga.

34.	Klik kanan untuk menyelesaikan poligon dan masukkan atribut. Ajaibnya poligon baru menyusut dan tersentak tepat ke batas poligon tetangga! Ini sangat berguna saat mendigitalkan batas kompleks di mana Anda tidak perlu tepat dan masih memiliki poligon yang benar secara topologi. Klik Toggle Editing untuk menyelesaikan pengeditan Parkslayer.

35.	Sekarang saatnya untuk mendigitalkan layer bangunan. Buat layer poligon baru bernama Buildingsdengan mengklik Layer Create Layer New GeoPackage Layer… icon dari Panels. Atur Buildings dan MuiltiPolygon . Pilih CRS sebagai . Klik Oke .EPSG:2193 - NZGD 2000

36.	Setelah Buildingslapisan ditambahkan, matikan lapisan Parksdan Roadsuntuk membuat peta topo dasar terlihat. Pilih Buildingslayer dan klik Toggle Editing .

37.	Mendigitalkan bangunan bisa menjadi tugas yang rumit, dan juga menantang untuk menambahkan simpul secara manual sehingga ujung-ujungnya tegak lurus dan membentuk persegi panjang. Kami akan menggunakan toolbar QGIS yang disebut Shape Digitizing untuk membantu tugas ini. Klik kanan pada ruang kosong mana pun di area bilah alat dan aktifkan file .Shape Digitizing Toolbar

38.	Aktifkan pengeditan dengan menekan ikon pensil Toggle Editing .

39.	Sekarang di bawah Add Rectangle dropdown pilih Add Rectangle from Extent tombol.

40.	Perbesar ke area dengan bangunan. Klik dan seret mouse untuk menggambar persegi panjang yang sempurna. Demikian pula, tambahkan bangunan yang tersisa.

41.	Anda akan melihat bahwa beberapa bangunan tidak vertikal, dan kita perlu menggambar persegi panjang pada sudut yang sesuai dengan tapak bangunan. Di bawah Add Rectangle dropdown pilih Add Rectangle from Center dan tombol Point .

42.	Perbesar ke area bangunan berbentuk wajik. Klik di tengah untuk menjatuhkan titik dan seret mouse untuk menggambar persegi panjang.

43.	Kita perlu memutar persegi panjang ini agar sesuai dengan gambar pada peta topo. Alat putar tersedia di toolbar Advanced Digitizing . Klik kanan pada area kosong pada bagian toolbar dan aktifkan toolbar Advanced Digitizing .

44.	Gunakan alat fitur Select Single untuk memilih poligon yang ingin Anda putar. Setelah alat Fitur Putar diaktifkan, Anda akan melihat garis bidik di tengah poligon. Klik tepat pada garis bidik itu dan seret mouse sambil menahan tombol klik kiri. Pratinjau fitur yang diputar akan muncul. Lepaskan tombol mouse saat poligon sejajar dengan tapak bangunan.

45.	Simpan hasil edit layer dan klik Toggle Editing setelah Anda selesai mendigitalkan semua bangunan. Anda dapat menyeret lapisan untuk mengubah urutan penampilannya. Tugas digitalisasi sekarang selesai. Anda dapat bermain dengan opsi penataan dan pelabelan di properti lapisan untuk membuat peta yang tampak bagus dari data yang Anda buat.

# Searching and Downloading OpenStreetMap Data (QGIS3)
1.	Cari dan instal plugin QuickOSM dari Repositori Plugin Resmi QGIS. Lihat Menggunakan Plugin untuk petunjuk tentang mengunduh plugin. Pastikan Anda memiliki kotak centang yang dipilih. Klik Tutup .
2.	Setelah terinstal, luncurkan plugin dari Vector QuickOSM QuickOSM… .
3.	Di tab Kueri cepat , Anda dapat menyetel filter untuk memilih subkumpulan. Atribut fitur peta dalam database OSM disimpan sebagai Tag . Tag diwakili dengan kunci dan nilai. Kuncinya adalah topik dan nilai adalah bentuk spesifik. Lihat halaman wiki Fitur Peta OSM untuk daftar lengkap tag untuk berbagai jenis fitur. Bilah diwakili menggunakan tag amenity:bardan pub dengan tag amenity:pub. Kami pertama-tama akan mengekstrak bilah. Pilih amenitysebagai Kunci dari menu drop-down.
4.	Pilih bardari menu tarik-turun Nilai .
5.	Kami dapat menghubungkan beberapa kueri dalam versi terbaru (v2.0.0 +) dari plugin QuickOSM. Klik tombol plus, bilah pemilihan kueri berikutnya akan muncul. Klik pada kotak pilihan pertama di mana kita bisa mendapatkan opsi Anddan Or. Dan hanya akan memilih fitur yang benar untuk semua kueri. Atau akan memilih semua fitur yang benar untuk salah satu kueri. Klik Oruntuk memilih fitur bar dan pub.
6.	Pilih amenitysebagai Kunci dari menu drop-down. Kemudian pilih pubdari menu tarik-turun Nilai .
7.	Masukkan Londonsebagai Masuk untuk membatasi pencarian di dalam batas kota.
8.	Luaskan bagian Lanjutan . Dalam model data OSM, fitur direpresentasikan menggunakan node, cara, dan relasi . Karena kami tertarik dengan fitur poin, Anda hanya dapat memilih Nodedan Points. Klik Jalankan kueri .
9.	Setelah kueri selesai, alihkan ke jendela utama QGIS. Anda akan melihat layer baru bernama amenity_bar_amenity_pub_Londonditambahkan ke panel Layers . Kanvas akan menunjukkan lokasi bar dan pub yang diekstrak.
10.	Buka tabel Atribut layer. Ada 2091fitur. Fasilitas kolom berisi kategori apakah fitur tersebut adalah pubatau bar. Dengan menggunakan kolom kategorikal ini, mari beri gaya pada layer kita.
11.	Klik icon panel Open the Layer StylingCategorized , pilih lalu di Value pilih amenitylalu klik Classify . Sekarang layer akan ditata dengan 2 warna yang menampilkan keduanya barsdan pubs.
12.	Sekarang klik kanan pada layer, Export Save Feature As… untuk mengekspor layer sebagai GeoPackage.
13.	Di kotak dialog Save Vector Layer as… , di Format pilih GeoPackage, di File name klik ...dan telusuri ke direktori tempat Anda ingin menyimpan data dan beri nama outputnya london.gpkg. Dalam nama Lapisan masukkan bar_and_pubs. Klik Oke .
14.	Sekarang lapisan GeoPackage london_bar_and_pubsakan ditambahkan ke kanvas.



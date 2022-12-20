## **Step-By-Step Visualisasi Data dengan Power BI**

Visualisasi data merupakan tahapan yang penting dalam analisis data. Ketika seorang data analyst ingin menyampaikan wawasan atau _insight_ dari data yang telah dianalisis, salah satu cara terbaik adalah dengan memvisualisasikannya. Seperti ungkapan populer “_A Picture is Worth a Thousand Words_“, yang dapat diartikan sebagai: “Sebuah gambar setara dengan ribuan kata”.

[Baca di Medium](https://medium.com/@ahmadilhamhabibi/step-by-step-visualisasi-data-dengan-power-bi-972e7853c287)

Pada ulasan kali ini saya akan membagikan langkah-langkah membuat visualisasi data pada Power BI. Mulai dari pengenalan Power BI, memasukkan data, mengolah data,membuat berbagai macam chart, serta membagikan hasil visualisasi.

**1. PENGENALAN POWER BI**
Power BI adalah kumpulan layanan, aplikasi, dan konektor perangkat lunak yang bekerja sama untuk mengubah sumber data yang tidak saling terkait menjadi wawasan yang koheren, mendalam secara visual, dan interaktif. Power BI memungkinkan Anda tersambung dengan mudah ke sumber data Anda, memvisualisasikan dan menemukan apa yang penting, dan membagikannya dengan siapa pun atau semua orang yang Anda inginkan. **(learn.microsoft.com)**

**2. GET AND TRANSFORM DATA**
Langkah pertama adalah memasukkan data yang ingin dianalisis kedalam Power BI. Pada menu home pilih Get Data, kemudian akan muncul banyak pilihan source data, diantaranya: Excel, csv, XML, JSON, Folder, Database, dan lain sebagainya. Kali ini saya akan mencoba mengambil data dari folder, excel, dan csv.

![Get data pada Power BI](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/2.1-GetData.jpg)

Setelah data diambil atau dimasukkan kedalam Power BI, selanjutnya kita bisa mentransformasikan atau mengedit data sesuai dengan kebutuhan analisis, seperti: menggabungkan kolom, menghapus kolom, memisahkan kolom, dan lain sebagainya.

**3. DATA MODELLING**
Ketika keempat tabel berhasil dibuat dan diload pada Power BI, kita bisa membuat visualisasi dari kolom-kolom yang ada pada tabel tersebut. Kita bisa membuat tabel dari kolom yang berbeda. Misalnya kolom _Category_ dari tabel **Products** dan kolom _Amount_ dari tabel **Sales**.

![Contoh visualisasi data yang belum terhubung](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/3.1-FalseData.jpg)

Contoh diatas menunjukkan nilai yang kurang tepat karena tabel-tabelnya belum terhubung satu sama lainnya. Jadi Power BI tidak bisa membedakan nilai dari Food, Baverages, dan Pastries. Tetapi langsung menampilkan nilai total dari ketiganya. Disinilah pentingnya data modelling, yaitu untuk menentukan hubungan antar tabel agar diperoleh nilai yang tepat.

![Data modelling saat belum ada hubungan antar tabel](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/3.2-DataModel.jpg)

Pada tab **Model**, kita bisa menentukan hubungan antar tabel. Caranya cukup sederhana, tinggal _drag and drop_ pada kolom yang ingin dihubungkan. Konsepnya sama dengan perintah **ON** pada **SQL JOIN**, yaitu menghubungkan kolom yang sama pada masing-masing tabel. Misalnya kolom _Product ID_ pada tabel **Sales** dihubungkan dengan kolom _ID_ pada tabel **Products**. Berikut contoh ketika data sudah dihubungkan.

![Data modelling saat sudah ditentukan hubungan antar tabel](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/3.3-DataModel.jpg)

Ketika tabel sudah terhubung, maka akan diperoleh visualisasi yang benar seperti berikut ini:

![Contoh visualisasi dataketika sudah terhubung](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/3.4-TrueData.jpg)

**4. _DATA ANALYSIS EXPRESSIONS_ (DAX)**
_Data Analysis Expressions_ (DAX) adalah kumpulan _syntax_ yang termasuk fungsi, operator, dan konstans yang dapat digunakan untuk membangun sebuah formula dan kalkulasi statistik untuk menghasilkan sebuah nilai atau hasil perhitungan baru. **(**[**sis.binus.ac.id**](https://sis.binus.ac.id/)**)**

DAX bisa berupa tabel atau kolom dalam tabel. Pada tab **DATA,** terdapat  pilihan untuk membuat _measure_, menambah kolom, dan menambah tabel baru.

Syntax DAX juga bisa menggunakan rumus seperti pada Microsoft Excel seperti SUM, COUNTROWS, CALCULATE, Date function, IF function, dan lain sebagainya.

Berikut contoh pembuatan kolom baru dengan nama _TotalRevenue_ dengan memanfaatkan rumus SUM pada kolom _Amount_.

![Membuat kolom TotalRevenue dengan rumus SUM](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/4.2-TotalRevenue.jpg)

Ketika sudah berhasil membuat DAX maka kita bisa memanfaatkannya berulang-ulang. Pada gambar diatas kita menggunakan kolom _TotalRevenue_ dengan kolom _Category_ dan kolom _MonthName_.

Selanjutnya buat kolom baru dengan nama _NoOfOrders_ dengan memanfaatkan rumus COUNTROWS pada tabel **Sales**. Kemudian tambahkan pada kedua visualisasi untuk melihat hasilnya.

Kita juga bisa menggunakan rumus CALCULATE yang mirip dengan rumus SUMIF pada Ms Excel. Misalnya ketika ingin menghitung Revenue pada saat weekend, maka kita menggunakan rumus CALCULATE dengan parameter TotalRevenue dan fungsi yang menunjukkan ketika weekend. Perhatikan gambar berikut.

![Membuat kolom TotalRevWeekend dengan rumus CALCULATE](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/4.4-Calculate.jpg)

**5. MEMBUAT VISUALISASI DATA**
Pada pembahasan sebelumnya kita sudah sedikit melihat visualisasi data, yaitu berupa _tabel_ dan _card_. Dalam Power BI terdapat banyak pilihan untuk memvisualisasikan data.  Pilihan visualisasi data pada Power BI terdapat pada panel Visualizations.

![Panel visualizations pada Power BI](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.1-PanelViz.jpg)

Untuk membuat visualisasi caranya cukup mudah. Tinggal klik pada jenis visualisasi yang diinginkan, kemudian sesuaikan Fields dengan kolom-kolom yang ingin divisualisasikan. Berikut beberapa contoh visualisasi yang sering digunakan:

**A. Card**
Card merupakan jenis visualisasi sederhana. Fungsinya untuk menampilkan angka. Biasanya digunakan ketika ingin menunjukkan satu jenis informasi saja. Ketika hanya ada satu atau dua kategori, penggunaan Card dirasa lebih cocok. Karena ketika dibuat dalam bentuk bar atau pie akan kehilangan fungsinya atau menjadin lebih sulit dipahami.
Berikut adalah contoh visusalisasi **Total Revenue** menggunakan jenis visualisasi Card. Untuk membuatnya cukup klik Card pada panel Visualisasi, kemudian isikan kolom _TotalRevenue_ pada Fields.

![Card](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.2-Card.jpg)

**B. Column Chart**
Selanjutnya adalah visualisasi yang sering dijumpai, yaitu Column Chart atau Bar Chart. Column Chart merupakan visualisasi yang mudah dipahami, kita tinggal membandingkan ujung dari masing-masing kolom untuk melihat data yang paling besar atau paling kecil.
Cara pembuatannya hampir sama dengan Card, namun ada perbedaan pada Fields. Fields berbeda-beda untuk setiap jenis visualisasi. Pada Column Chart Fields berisi X-axis, Y-axis, Legend, Tooltips, dan beberapa fields lainnya.

![Column](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.3-Column.jpg)

**C. Map**
Map digunakan untuk membuat visualisasi berdasarkan letak geografis. Pada Power BI setidaknya ada tiga pilihan untuk membuat map, yaitu Map, Filled Map, dan Shape Map.
Pilih Map kemudian sesuaikan Fields yang ada. Location diisi dengan kolom _Country_, maka akan otomatis dibuatkan peta berdasarkan data tersebut. Latitude dan Longitude bisa dikosongi karena sudah ada Location. Bubble Size diiisi dengan _TotalRevenue_ untuk melihat perbedaan revenue di tiap negara. Terakhir sesuaikan format pada Map. Maka kurang lebih akan menjadi seperti pada gambar berikut:

![Map](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.4-Map.jpg)

**D. Slicer**
Slicer berfungsi untuk memfilter visualisasi sesuai dengan kondisi yang diberikan. Jika pada PivotTable Slicer merupakan fitur terpisah dari Pivot Chart, pada Power BI Slicer merupakan salah satu jenis visualisasi data.
Cara membuatannya sama dengan visualisasi lainnya. Klik ikon Slicer kemudian sesuaikan Fields yang ada. Slicer biasanya diisi dengan kolom dengan tipe _Date Time_.
Pada contoh diatas input Fields diisi dengan kolom _Date_. Kemudian pada pojok kanan atas terdapat pilihan untuk menyesuaikan Slicer, yaitu: Between, Before, After, List, Dropdown, Relative Date dan Relatif Time. Namun jika Fields diisi dengan kolom _Year_, maka pilihannya akan berubah menjadi: Between, List, Dropdown, Less than or equal to, dan Greater than or equal to.

![Slicer](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.5-Slicer.jpg)

**E. Key Performance Indicator** (**KPI)**
Visualisasi Key Performance Indicator (KPI) hampir mirip dengan Card. Namun pada KPI terdapat warna yang menunjukkan pencapaian terhadap target tertentu. Warna hijau menenjukkan telah mencapai target sedangkan warna merah menunjukkan belum mencapai target.
Target ini ditentukan pada panel Fields. Disini kita menentukan Value, Trend, dan Target. Perhatikan gambar berikut:

![KPI](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.6-KPI.jpg)

**F. Line Chart**
Line Chart berfungsi untuk melihat _trend_ suatu keadaan terhadap waktu. Misalnya melihat trend penjualan pada periode tertentu, memonitor harga secara real time, dan lain sebagainya.
Pada Line Chart setidaknya kita harus menentukan panel Fields yang berisi X-axis, Y-axis, Legend, serta Tooltips.

![Line](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.7-Line.jpg)

**G. Matrix**
Visualisasi selanjutnya adalah Matrix yang memiliki fungsi mirip dengan Pivot Table pada Ms. Excel. Pada Matrix kita bisa membuat tabel berdasarkan kolom-kolom tertentu.
Ketika membuat Matrix kita harus menyesuaikan panel Fields berupa Rows, Columns, dan Values.

![Matrix](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.8-Matrix.jpg)

**H. Table**
Visualisasi terakhir pada pembahasan kali ini adalah tabel. Mirip dengan Matrix tetapi kita hanya menentukan kolom-kolomnya saja. Kita bisa mengembangkan tabel dengan menerapkan filter yang mirip dengan _Conditional Formatting._
Pada contoh diatas tabel berisi tiga kolom yaitu _Profuct, TotalRevenue,_ dan _NoOfOrders_. Kemudian dilakukan filtering untuk menampilkan lima product dengan _TotalRevenue_ tertinggi.

![Table](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/5.8-Tabel.jpg)

**6. REPORT DESIGN**
Setelah membuat berbagai visualisasi langkah selanjutnya adalah membuat desain laporan agar enak dipandang. Pada proses desain biasanya kita menambahkan _shape_ untuk menambahkan header, _Text box_ untuk menambah teks atau judul laporan, serta mengubah tema atau warna.

Pertama, tambahkan shape dan box, kemudian sesuaikan warna dan tulisan agar lebih informatif. Pada menu Insert terdapat pilihan untuk menambahkan _Text box, Bottom, Shapes,_ dan _Images_.

![Element](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/6.1-Shape.jpg)

Tambahkan Shape, pilih Rectangles untuk menambahkan bangun segi empat. Kemudian sesuaikan posisinya pada bagian atas agar berfungsi sebagai header.

![Shape](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/6.2-Ractangles.jpg)

Tambahkan _Text box_ untuk memberi judul pada header. Pada menu Insert, pilih _Text box_, kemudian sesuaikan dengan judul laporan.

![Text Box](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/6.3-TextBox.jpg)

Ketika ada visualisasi yang bertumpuk seperti _Shape, Text box,_ dan _Slicer_ seperti di atas, kita perlu menyesuaikan urutannya pada panel _Selection_. Agar semua visualisasi dapat dilihat dengan baik. _Slicer_ dan _Text box_ harus berada diatas _Shape_. Perhatikan gambar berikut:

![Selection](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/6.4-Selection.jpg)

**7. EDIT INTERACTION**
Visualisasi pada Power BI dibuat agar bisa interaktif dengan penggunannya. Data yang ditampilkan bisa berubah-ubah sesuai dengan interaksi dengan pengguna.

![Edit In](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/7.1-EditInteraction.jpg)

Pada contoh diatas penggunan mengklik **Map** pada buble USA, maka visualisasi yang lainnya seperti **Total Revenue, Number Of Order,** serta **Column Chart** juga menunjukkan data USA saja.

Interaksi ini merupakan fitur yang sangat berguna, namun kita juga harus menyesuaikan data mana saja yang bisa diubah agar pengguna tidak kehilangan informasi penting dari laporan yang kita buat.

Klik visualisasi yang ingin kita edit interaksinya. Pada menu **Format**, pilih _Edit Interactions_. Kemudian ada dua pilihan pada visualisasi lainnya, pilih **Filter** untuk membuat visulisasi yang interaktif atau pilih **None** untuk mematikan fitur interaktif.

![Edit Interction](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/7.2-EditInteraction.jpg)

**8. PUBLISH AND SHARE REPORT**

Ketika selesai membuat laporan, langkah selanjutnya adalah membagikan laporan tersebut kepada pihak yang memerlukan. Pada Power BI kita bisa mempublish laporan ke Power BI Service. Pada **Home** tab, pilih **Publish**.

![Publish](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/8.1-Publish.jpg)

Ketika telah berhasil di Publish maka akan muncul link untuk menuju Power BI service. Disini kita bisa melakukan interaksi dengan filter yang telah dibuat sebelumnya.

![Final Dashboard](https://github.com/ahmadilhamhabibi/Power-BI/blob/main/Images/8.2-Publish.jpg)

Selain itu, ada pilihan lain untuk membagikan hasil laporan dari Power BI, yaitu dengan cara ekspor ke Power Point atau PDF. Kita juga bisa membagikan link atau embed pada email untuk versi Power BI Pro.

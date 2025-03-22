## ETL Project Description

Proyek ini melakukan ETL pada dua file CSV yang berisi data polusi udara dari 8 kota antara tahun 2017 dan 2020.


<b>Tools: Bigquery, Colab, Python, Pandas.</b>

### Extract 
melakuakn load data yang diambil dari bigquery

### Transform
Menghapus kolom yang tidak perlu dan mengganti nama kolom Count pada setiap dataframe, Count_o3 dan Count_pm25. Saya kemudian menggabungkan kedua df ini menggunakan penggabungan kiri pada kolom Tanggal, Negara, dan Kota di masing-masing df, menghasilkan satu df dengan jumlah o3 dan pm25 untuk setiap hari di setiap kota.

### Load 
Membuat skema, menggunakan tanda kutip untuk nama kolom dengan huruf besar. Menggunakan Bigquery, membuat database ETL dan di dalamnya, tabel bernama merge_counts. Saya kemudian memuat data ke dalam database menggunakan new_df.to_gbq. 

# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding
### Latar Belakang Bisnis
Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dengan lebih dari 1000 karyawan yang tersebar di berbagai wilayah. Walaupun perusahaan ini sudah cukup besar dan mapan, mereka masih menghadapi masalah serius dalam pengelolaan sumber daya manusia. Salah satu isu utama adalah tingginya tingkat **attrition** atau perputaran karyawan yang mencapai lebih dari 10%. Hal ini menjadi indikator adanya kesulitan dalam mempertahankan karyawan, yang dapat berdampak negatif pada produktivitas, biaya rekrutmen, serta kelangsungan operasional perusahaan.

### Permasalahan Bisnis 
Permasalahan bisnis utama yang akan diselesaikan dalam proyek ini adalah:
* Mengidentifikasi faktor-faktor utama yang memengaruhi tingginya attrition rate di Jaya Jaya Maju.

### Cakupan Proyek
Proyek ini mencakup:
* Melakukan analisis data untuk memahami pola dan tren yang berkaitan dengan attrition.
* Membangun model machine learning untuk menentukan fitur-fitur penting yang dapat membantu mencegah attrition karyawan.

### Persiapan dan Setup
- **Sumber Data**: Data karyawan diperoleh dari [repositori GitHub Dicoding](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee).  Dataset ini adalah Dataset Karyawan Jaya Jaya Maju sesuai dengan instruksi dari submission proyek ini.
- **Setup Environment**:  
   1. **Menjalankan `notebook.ipynb`**
   - Pastikan dependensi, packages, library yang dibutuhkan sudah tersedia (lihat file `requirements.txt` untuk melihat dependensi yang dibutuhkan).
   - Jalankan seluruh isi file `notebook.ipynb` menggunakan Google Colab/Jupyter Notebook untuk melihat hasil analisis data, temuan, dan insight yang diperoleh.
   2. **Menjalankan Dashboard**:
   Untuk melihat isi dashboard secara langsung, dapat menggunakan **metabase** dengan bantuan Docker (pastikan Docker sudah terinstall).
   - Jalankan perintah berikut:
      ```
      docker pull metabase/metabase:v0.46.4
      ```
   - Jalankan container Metabase menggunakan perintah:
      ```
      docker run -p 3000:3000 --name metabase metabase/metabase
      ```
   - Login ke Metabase menggunakan username dan password berikut:
      ```
      username: root@mail.com
      password: root123
      ```
## Business Dashboard
Hasil analisis data divisualisasikan dalam bentuk dashboard untuk membantu tim HR memantau dan memahami fenomena attrition karyawan. Elemen-elemen yang disertakan dalam dashboard meliputi:
* **Attrition Rate** secara keseluruhan sebagai indikator tingkat turnover karyawan.
* **Jumlah total karyawan (Total Employee)** yang masih aktif dan yang sudah keluar, disajikan dalam grafik yang mudah dipahami.
* **Faktor-faktor utama yang berkaitan dengan attrition**, antara lain:
  * Karyawan yang melakukan **lembur (OverTime)** memiliki risiko keluar lebih tinggi (Attrition by OverTime).
  * karyawan laki-laki memiliki tingkat attrition yang lebih tinggi dibandingkan perempuan (Attrition by Gender). 
  * Karyawan dengan **status perkawinan single** menunjukkan kecenderungan keluar yang lebih besar (Attrition by MaritalStatus).
  * Posisi **Sales Representative** dan **Laboratory Technician** memiliki tingkat attrition yang relatif tinggi (Attrition by JobRole).
* **Faktor-faktor yang berperan dalam mengurangi attrition**, seperti:
  * Tingkat **Job Level** yang lebih tinggi terkait dengan tingkat retensi yang lebih baik (Attrition by JobLevel).
  * Kepuasan lingkungan kerja (**Environment Satisfaction**) yang tinggi membantu menurunkan risiko keluar (Attrition by EnvironmentSatisfaction).
  * Level opsi saham (**Stock Option Level**) yang lebih tinggi juga berkontribusi pada karyawan yang bertahan (Attrition dan Stock Option Level).
    
![Dashboard](gambar/Business%20Dashboard%20Ersyafin.jpg)

## Conclusion
Berdasarkan hasil analisis data dan visualisasi pada dashboard interaktif, dapat disimpulkan bahwa attrition karyawan di perusahaan dipengaruhi oleh berbagai faktor yang bersifat positif maupun negatif terhadap keputusan karyawan untuk keluar. Faktor seperti OverTime, status pernikahan Single, dan frekuensi perjalanan bisnis memiliki korelasi positif terhadap attrition, yang berarti kondisi tersebut berkontribusi pada peningkatan risiko karyawan keluar. Sebaliknya, faktor seperti JobLevel, StockOptionLevel, dan EnvironmentSatisfaction memiliki korelasi negatif, artinya faktor-faktor ini cenderung menahan karyawan untuk tetap tinggal.

Pemahaman terhadap pola ini sangat penting untuk membantu tim HR merancang strategi retensi yang lebih tepat sasaran, sehingga dapat menurunkan tingkat turnover dan meningkatkan stabilitas organisasi.

## Rekomendasi Action Items
Berikut adalah beberapa rekomendasi tindakan yang dapat dilakukan perusahaan untuk mengurangi attrition rate:

1. **Action Item 1:** Mengurangi lembur (OverTime), karena menjadi faktor paling kuat yang berkorelasi positif terhadap attrition. Perusahaan dapat mengatur ulang beban kerja, menambah tenaga kerja, atau memberikan kompensasi dan waktu istirahat yang seimbang untuk mengurangi tekanan kerja berlebih.
2. **Action Item 2:** Meningkatkan keterlibatan dan retensi karyawan lajang (MaritalStatus\_Single) dengan menyediakan program engagement sosial, mentoring, dan komunitas internal yang membangun rasa memiliki terhadap perusahaan.
3. **Action Item 3:** Melakukan pengawasan khusus pada posisi *Sales Representative* dan *Laboratory Technician*, karena kedua job role ini memiliki korelasi tinggi terhadap attrition. Bisa dilakukan dengan memberikan jalur karier yang lebih jelas, insentif khusus, atau pelatihan pengembangan diri.
4. **Action Item 4:** Meningkatkan peluang promosi dan mobilitas karier, khususnya bagi karyawan dengan *YearsSinceLastPromotion* yang tinggi. Ini penting untuk menjaga motivasi dan mengurangi risiko kehilangan talenta.
5. **Action Item 5:** Memberikan insentif seperti opsi saham (StockOptionLevel) sebagai bentuk apresiasi jangka panjang terhadap kontribusi karyawan, yang terbukti dapat menurunkan tingkat attrition secara signifikan.
6. **Action Item 6:** Menjaga kepuasan terhadap lingkungan kerja (*EnvironmentSatisfaction*) melalui perbaikan fasilitas fisik, budaya kerja yang suportif, serta sistem umpan balik karyawan yang aktif dan responsif.







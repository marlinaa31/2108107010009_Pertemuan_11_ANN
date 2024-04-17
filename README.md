# Tugas 3 Machine Learning

## About Me
Nama: Marlina                                                                        
NPM: 210810701009

Repository ini dibuat untuk menyelesaikan tugas INF540 Pembelajaran Mesin dengan menerapkan Jaringan Saraf Tiruan (ANN) pada dataset breast cancer dan data bank churn untuk dilakukan klasifikasi serta dataset mobile price untuk dilakukan regresi.

Materi bacaan: 
- https://www.megabagus.id/deep-learning-artificial-neural-networks/ (halaman 1 - 7)
- ⁠⁠https://www.megabagus.id/deep-learning-artificial-neural-networks-aplikasi (halaman 1 - 4)

Pahami isi dari kedua artikel tersebut dan kerjakan:
- Contoh pada artikel kedua menggunakan tensorflow pada python environment
- ⁠Tugas 2 sebelumnya menggunakan SVM, kerjakan dengan menggunakan ANN pada python environment yang sama

Kumpulkan kedua tugas tersebut menggunakan repository pada github dengan nama repository: NPM_Pertemuan_11_ANN. Repository tersebut berisi:
- Dataset sebelum dipreprocessing (format csv)
- ⁠Kode python yang memuat process preprocessing, training, testing dan perhitungan akurasi
- ⁠File requirements.txt yang berisi library yang digunakan
- ⁠File README.md yang berisi penjelasan tentang kedua tugas yang dikerjakan beserta perbandingan akurasi SVM dan ANN

## Klasifikasi

Source dataset: https://www.kaggle.com/datasets/erdemtaha/cancer-data/data

Atribut:
* radius_mean
* texture_mean
* perimeter_mean
* area_mean 
* smoothness_mean
* compactness_mean 
* concavity_mean
* concave points_mean

## Studi Kasus
- Dataset ini berisi data tentang kanker untuk memprediksi apakah kanker bersifat "M" (Ganas) atau "B" (Jinak). Semua atribut ini Mewakili nilai rata-rata dari visual kanker/penampilan kanker

## Regresi

Source dataset: https://www.kaggle.com/datasets/mohannapd/mobile-price-prediction/data

Atribut:
- **Product_id**: Merupakan identifikasi unik untuk setiap produk.
- **Price**: Merupakan harga produk dalam satuan tertentu (mungkin dalam mata uang tertentu).
- **Sale**: Mungkin merupakan penjualan atau jumlah penjualan produk tersebut.
- **weight**: Merupakan berat produk, umumnya dalam satuan tertentu (misalnya gram).
- **resolution**: Merupakan resolusi layar produk.
- **ppi**: Pixels Per Inch (PPI) merupakan ukuran kepadatan piksel layar, yang dapat mempengaruhi kualitas tampilan.
- **cpu core**: Jumlah inti (core) pada prosesor.
- **cpu freq**: Frekuensi prosesor dalam satuan tertentu (mungkin GHz).
- **internal mem**: Merupakan ukuran memori internal produk dalam satuan tertentu (misalnya GB).
- **ram**: Merupakan ukuran memori RAM produk dalam satuan tertentu (misalnya GB).
- **RearCam**: Resolusi kamera belakang produk.
- **Front_Cam**: Resolusi kamera depan produk.
- **battery**: Kapasitas baterai produk dalam satuan tertentu (misalnya mAh).
- **thickness**: Ketebalan produk dalam satuan tertentu (misalnya cm).

## Studi Kasus 

Studi kasus dataset ini adalah membangun model untuk memprediksi harga produk berdasarkan fitur-fiturnya. Misalnya, kita ingin memprediksi harga produk berdasarkan resolusi layar, kepadatan piksel (PPI), jumlah inti prosesor, ukuran memori internal, dan lain-lain.

## Source Code

- [Contoh ANN pada Artikel](https://github.com/marlinaa31/2108107010009_Pertemuan_11_ANN/blob/main/ANN_Article2.ipynb)
- [ANN_Classification.ipynb](https://github.com/marlinaa31/2108107010009_Pertemuan_11_ANN/blob/main/2108107010009_ANN_Classification.ipynb)
- [ANN_Regression.ipynb](https://github.com/marlinaa31/2108107010009_Pertemuan_11_ANN/blob/main/2108107010009_ANN_Regression.ipynb)

## Cara Menjalankan Code

1. Making virtual environment: 
```bash
python3 -m venv env_name
```
2. Activate virtual environment:
```bash
source env_name/bin/activate
```
3. Install requirements :
```bash
pip install -r requirements.txt
```
4. Run all the code cell sequentially

## Perbandingan Hasil SVM dan ANN

Tugas SVM dapat dilihat [disini](https://github.com/marlinaa31/Tugas-2-Machine-Learning/tree/main) 

### Klasifikasi
1. SVM model dengan kernel RBF berhasil memprediksi dengan akurasi 91% dan untuk Linear Kernel 94%.
2. ANN model dengan 4 layer juga mendapatkan akurasi 95%

### Regresi
1. SVM model dengan polynomial derajat 3 memperoleh nilai mse MSE: 0.4037759076223635
2. ANN model dengan 3 layer  (satu input layer, hidden layer, dan output layer) menggunakan loss mse mendapat nilai 0.4005

## Kesimpulan
Dari hasil yang diberikan, kita dapat membuat kesimpulan sebagai berikut:

### Klasifikasi:
Dari perbandingan di atas, terlihat bahwa model ANN dengan 4 layer memiliki akurasi yang paling tinggi, yaitu 95%. Sedangkan, SVM dengan kernel Linear memiliki akurasi tertinggi kedua dengan 94%, diikuti oleh SVM dengan kernel RBF dengan akurasi 91%.

### Regresi:
Dari hasil tersebut, model ANN dengan 3 layer memberikan nilai MSE yang sedikit lebih rendah (0.4005) dibandingkan dengan SVM dengan polynomial derajat 3 (0.4037759076223635).

Dalam kedua kasus klasifikasi dan regresi, terlihat bahwa model ANN memiliki kinerja yang kompetitif atau bahkan lebih baik dibandingkan dengan SVM. Hal ini mungkin disebabkan oleh kemampuan ANN dalam memahami pola-pola yang kompleks dan non-linear dalam data, yang mungkin tidak dapat ditangkap dengan baik oleh SVM.



















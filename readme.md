
# PENGENALAN PLAT NOMOR

## Gisani Miftahul Rahma

Proyek ini dibuat untuk memenuhi tantangan uji Synapsis.

### TAHAPAN PROYEK

Dalam pengembangan proyek ini, langkah-langkah berikut dilakukan:

1. **Akuisisi Data:**
   - Pada tahap ini, pengumpulan data untuk pelatihan dilakukan.
   - Proyek menggabungkan dataset dari Kaggle dan Roboflow.
   - Jumlah total data yang diperoleh adalah 5508, dapat diakses [di sini](https://app.roboflow.com/ds/33Exggt3Nh?key=HCS4k4phui).

2. **Preprocessing Data:**
   - Pada tahap ini, beberapa proses diterapkan pada data mentah untuk membuatnya siap digunakan.
   - Proses tersebut meliputi:
     - Remapping: Untuk membuat label seragam.
     - Mengubah Ukuran: Menyamakan dimensi gambar menjadi 640x640.

3. **Augmentasi Data:**
   - Proses ini bertujuan untuk memperkaya data dengan berbagai teknik augmentasi, termasuk:
     - Rotasi: Antara -15° dan +15°.
     - Shear: ±15° Horizontal, ±15° Vertikal.
     - Noise: Hingga 5% dari piksel.

4. **Pelatihan:**
   - Proses pelatihan dilakukan untuk melatih model deteksi objek.
   - Deteksi objek pada plat nomor dilakukan menggunakan YOLO V8.
   - Kode untuk proses pelatihan dapat ditemukan dalam file "Licence_Plate_Detection_YOLO_V8.ipynb".

5. **Pengenalan Gambar:**
   - Hasil deteksi objek pada plat nomor yang dibuat selanjutnya digunakan untuk pengenalan karakter menggunakan EasyOCR.
   - File untuk proses ini dapat ditemukan dalam file "Synapsis_Licence_Recognition.ipynb".

### CARA PENGGUNAAN

Program ini dapat dijalankan pada komputer lokal menggunakan Jupyter Notebook. Untuk menjalankannya, Anda dapat menjalankan file "Synapsis_Licence_Recognition.ipynb".

```python
!git clone https://github.com/gisagisa/plate_rec2.git
```

```python
pip install -r requirements.txt
```
Anda mungkin perlu menyesuaikan kode di atas sesuai dengan direktori file "requirements.txt" yang telah di-clone pada langkah sebelumnya.

Selanjutnya, Anda dapat menggunakan perintah berikut untuk menjalankan program:
```python
!python predictWithOCR.py model='C:\Users\user\anaconda3\envs\yolo-gpu\plate-det\best.pt' source=0
```
Kode di atas juga dapat disesuaikan dengan direktori file yang telah di-clone.





> Written with [StackEdit](https://stackedit.io/).

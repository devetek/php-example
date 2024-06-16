## Description

Contoh aplikasi PHP untuk dapat di release melalui [dPanel](https://cloud.terpusat.com/). Lihat pengaturan yang ada di dalam folder `.devetek`.

## Komponen Utama

Di dalam pengaturan YAML, ada 3 komponen utama yang perlu diperhatikan untuk dapat melakukan release aplikasi melalui dPanel:

### setup

Komponen ini digunakan untuk memvalidasi ketersediaan dependency aplikasi untuk dapat berjalan. Digunakan untuk bahasa pemrograman interpreter seperti (PHP, Python, Rubby, Javascript, etc).

### build

Komponen ini digunakan untuk medefinisikan step-step yang akan dijalankan selama proses build. Menggunakan working directory dimana aplikasi di tarik dari sumber (github, bitbucket, gitlab, etc). Terdapat 2 definisi yang tersedia:

- cmd - Digunakan untuk mengeksekusi command yang dimasukkan
- archive - Digunakan untuk melakukan archiving target yang telah didefinisikan. Untuk didistribusikan ke penyimpanan sehingga dapat digunakan untuk banyak resource

### run

Komponen ini digunakan untuk mendefinisikan pengaturan runtime aplikasi. Komponen utama yang perlu diperhatikan diantaranya:

- name - Digunakan untuk membuat nama service di dalam mesin, hanya diperbolehkan menggunakan "-" sebagai pemisah kata
- description - Digunakan untuk membuat deskripsi aplikasi agar lebih mudah dimengerti
- command - Perintah yang akan digunakan untuk menjalankan aplikasi, relative terhadap working directory dimana aplikasi ditarik dari sumber (github, bitbucket, gitlab, etc).

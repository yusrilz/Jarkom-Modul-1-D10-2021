# Praktikum Modul 1 Jarkom 2021 (Kelompok D10)

#### Nama anggota kelompok:
- Mohammad Faderik I H (05111940000023)
- Farhan Arifandi (05111940000061)
- Yusril Zubaydi (05111940000160)


## Soal 1
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!

**Jawaban:**

- Menggunakan display filter `http.host == ichimarumaru.tech`
![Soal 1.1](https://user-images.githubusercontent.com/70105993/134631184-1b8c5453-15ff-47a4-89e2-80c308eeaa89.jpg)

- Klik kanan salah satu paket > Follow > HTTP Stream\
![Soal 1.2](https://user-images.githubusercontent.com/70105993/134631525-7e7d5bbe-a7ed-4b12-b4e7-a8a3ad3be004.jpg)

- Diperoleh webserver yang digunakan yaitu **NGINX 1.18.0 (Ubuntu)**


## Soal 2
Temukan paket dari web-web yang menggunakan basic authentication method!

**Jawaban:**

- Menggunakan display filter `http.authbasic`, diperoleh 3 paket
![Soal 2](https://user-images.githubusercontent.com/70105993/134631661-d62dd7d5-2a9c-48fa-9515-1bfbfcffaa9b.jpg)


## Soal 3
Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!

**Jawaban:**

- Menggunakan display filter `http.host == basic.ichimarumaru.tech`, diperoleh paket-paket yang berasal dari basic.ichimarumaru.tech dan menggunakan basic authentication method

- Klik salah satu paket, buka bagian Hypertext Transfer Protocol > Authorization > Credentials, didapatkan username:password = **kuncimenujulautan:tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN**
![Soal 3.1](https://user-images.githubusercontent.com/70105993/134632008-62ece5c4-70f1-47dd-8495-240e81abb747.jpg)

- Setelah login ke basic.ichimarumaru.tech dengan username dan password tersebut, diperoleh pertanyaan "Sebutkan urutan konfigurasi pengkabelan T568A!"
  - Jawaban: Putih hijau, hijau, putih oranye, biru, putih biru, oranye, putih cokelat, cokelat
![Soal 3.2](https://user-images.githubusercontent.com/70105993/134632330-b688e906-4ba9-4773-be79-6260eb4e01d1.jpg)


## Soal 4
Temukan paket mysql yang mengandung perintah query select!

**Jawaban:**

- Menggunakan display filter `mysql contains select`, diperoleh 2 paket
![Soal 4](https://user-images.githubusercontent.com/70105993/134632891-3241d8f0-39e4-49fd-840b-8a1fa8735569.jpg)


## Soal 5
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!

**Jawaban:**

- Menggunakan display filter `mysql.query contains INSERT`, diperoleh 1 paket

- Klik paket, buka bagian MySQL Protocol > Request Command Query, didapatkan statement INSERT yang mengandung informasi username yaitu ‘akakanomi’, dan password yaitu ‘pemisah4lautan’
![Soal 5.1](https://user-images.githubusercontent.com/70105993/134633100-6eeacb38-4c8f-44a0-9911-405941ed3083.jpg)

- Setelah login ke portal.ichimarumaru.tech dengan username dan password tersebut, diperoleh pertanyaan "Sebutkan urutan konfigurasi pengkabelan T568B!"
  - Jawaban: Putih oranye, oranye, putih hijau, biru, putih biru, hijau, putih cokelat, cokelat
![Jarkom-Modul-1-D10-202152](https://user-images.githubusercontent.com/70105993/134633547-f290f301-1a98-4f69-8828-ff2bea0893f1.jpg)


## Soal 6
Pertanyaan

**Jawaban:**


## Soal 7
Pertanyaan

**Jawaban:**


## Soal 8
Pertanyaan

**Jawaban:**


## Soal 9
Pertanyaan

**Jawaban:**


## Soal 10
Pertanyaan

**Jawaban:**


## Soal 11
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

**Jawaban:**
Untuk mendapatkan paket yang *berasal* dari port 80, dapat menggunakan capture filter `src port 80`. `src` berfungsi untuk mendapatkan paket yang hanya berasal dari sumber tertentu.
![alt text](https://cdn.discordapp.com/attachments/769183322147389460/891293663756427314/unknown.png)

## Soal 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Jawaban:**
Untuk mendapatkan paket yang mengandung port 21, dapat menggunakan capture filter `port 21`.
![alt text](https://cdn.discordapp.com/attachments/769183322147389460/891295131276308560/unknown.png)

## Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

**Jawaban:**
Untuk mendapatkan paket yang menuju port 443, dapat menggunakan capture filter `dst port 443`. `dst` berfungsi untuk mendapatkan paket yang hanya menuju tujuan tertentu.
![alt text](https://cdn.discordapp.com/attachments/769183322147389460/891293667241889874/unknown.png)

## Soal 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

**Jawaban:**
Untuk mendapatkan paket yang tujuannya ke kemenag.go.id, dapat menggunakan capture filter `dst host kemenag.go.id`
![alt text](https://cdn.discordapp.com/attachments/769183322147389460/891293662863056896/unknown.png)

## Soal 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

**Jawaban:**
Untuk mendapatkan paket yang berasal dari IP, pertama, saya mencari tahu IP saya menggunakan `ipconfig` pada command prompt, setelah itu menggunakan capture filter `ip src (IP)`
Di sini IP saya 192.168.82.178, sehingga capture filternya menjadi `ip src 192.168.82.178`.
![alt text](https://cdn.discordapp.com/attachments/769183322147389460/891293667485171712/unknown.png)

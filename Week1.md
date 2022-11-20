# WEEKLY 1
## Unix Command Line
- ### CLI (Command Line Interface).
    Program agar user dapat melakukan perintah kepada 
    komputer

- ### Shell
    Jadi,shell ini adalah program yang menerima perintah tadi dan akan diteruskan kepada sistem

- ### Terminal
    Pada terminal ini lah tempat mengetikkan perintah dari shell tadi

- ### File System 
    Cara sistem operasi mengatur file dan direktori nya dalam bentuk struktur yang mirip dengan pohon

- ### Command
    - pwd, untuk melihat di directory mana kita sedang berada 
    - dir, untuk melihat directory
    - cd, untuk pindah directory
    - ls, untuk melihat isi file di dalam directory
    - touch, untuk membuat file 
    - cp, untuk menyalin file
    - mv, untuk memindahkan file
    - mkdir,untuk membuat directory
    - head,tail,cat,untuk melihat beberapa line awal dari file text 
    - rm, untuk menghapus file directory

command yang ditambahkan -R akan berubah perintah menjadi directory,yang artinya ketika kita membuat commnad mv -R perintah menjadi memindahkan directory

&nbsp;

## GIT dan Github
- ### Git 
    Git adalah tools yang digunakan pada developer untuk mengerjakan dan mengembangkan software bersama sama.Fungsi utama dari git ini adalah melacak perubahan dari yang terjadi dari suatu folder,maupun file.

- ### Github
    Github adalah repo dari git tersebut,kita dapat menyimpan hasil codingan kita pada github ini

- ### Command Github
    - Untuk membuat repo baru,kita harus membuat command git init (nama_proyek)
    - Untuk melakukan commit atau menyimpan perubahan version control pada git,kita harus membuat command git commit -m"nama commit"
    - Untuk mempublish file kita ke github,tambahkan command git push origin
    - Melakukan cloning dari github ke penyimpanan local kita tambahkan git clone

&nbsp;

## HTML
HTML merupakan kerangka dalam membuat sebuah website.Beberapa Tag yang ada dalam HTML :

- #### Tag untuk menampilkan teks,
    Abaikan tanda (-) pada sebuah tag
    - **Heading**,heading 1 akan membuat font besar,sampai yang terkecil yaitu heading 6 dgn tag<-h1>teks<-/h1>
    - **Paragraph**,membuat paragrph dalam html cukup membuat tag <-p><-/-p>
    - **Link/Anhcor**,buat tag<-a><-/a>,contoh<-a href="https://google.com">Google</-a>
    - **Span**,memiliki fungsi untuk mengelompokkan tulisan dalam satu baris,biasanya digunakan dalam css untuk membuat style dalam satu baris,contoh <-p>mobil itu berwarna <-span style="color:blue"> merah</-span></-p>,hasilnya sbg berikut <p>Kucingku bermata <span style="color:red"> merah</span></p>
    - **Bold**,tambahkan tag <-b><-/b> atau <-strong><-/strong>
    - **Italic**,tambahkan tag <-i><-/i> atau <-em><-/em>
    - **List**,list yang terurut(1,2,3)dan list yg tidak berurut,yg berbentuk bulatan,untuk yang teurut <-ol><-/ol> dan list tak terurut <-ul><-/ul>

&nbsp;
- #### Tag untuk Multimedia 
    - **Gambar**,jika ingin menambahkan gambar buat tag
    <-img src="https://bit.ly/3j6eb3B" alt="Cat" />
    src adalah dmn letak dari gambar yang ingin ditampilkan,sedangkan utk alt adalah informasi alternatif jika gambarnya gagal,hasilnya
    <img src="https://bit.ly/3j6eb3B" alt="Cat" />
    - **Audio**,<-audio controls src="link-ke-file-audio"><-/audio>,control diatas berfungsi agar audio di website kita bs diplay dan dipause,sedangkan jika kita ingin audionya keputar otomatis,buat autoplay dan looping jika ingin mengulang ulang audio nya.
    - **Vidio**,tambahkan tag <-video width="320" height="240" Controls>,sama seperti audio,fungsi controls untuk ngeplay dan ngepause.  

&nbsp;
- #### Tag Membuat Tabel
    - **<-table>** element utama
    - **<-tr>** membuat baris dalam table
    - **<-td>** container (wadah) dari data yang kita mau isi di dalam 

untuk mendeploy web atau html yang telah kita buat,kita bisa menggunakan layanan server dari netlify
&nbsp;

## CSS
CSS atau Cascading Style Sheets,merupakan cara agar tampilan website yang kita buat menarik,ibaratnya manusia html adalah tubuh dan kerangka kita dan css adalah pakaian kita dan perhiasaan yang kita pakai,cara menggunakan 
> css ada 3 yaitu
(abaikan tanda - dalam tag)
- #### **Inline**,Penggunaan inline ini langsung pada baris HTML nya  
     <-p style="color:red">Tulisan ini berwarna merah<-/p>
- #### **Internal**,Penggunaan internal ini didalam file HTML itu sendiri,menggunakan tag <-style> yang diletakkan dalam tag <-head>
`

     
     <!DOCTYPE html>
     <html>
       <head>
         <title>Website Pertamaku</title>
         <style>
           body {
             background-color: yellow;
           }
           h1 {
             color: blue;
           }
           p {
             color: red;
           }
         </-style>
       </head>
       <body>
         <h1>Website Pertamaku</h1>
         <p>Selamat Datang</p>
       </body>
     </html>'
''
    hasilnya adalah
    ![](internal-css.jpg)

- #### Eksternal CSS,untuk eksternal css ini kita akan membuat file yang berbeda dari html dan menyisipkan file css nya tadi kedalam file html dengan menggunakan tag <-link rel="stylesheet" href="nama file.css" />,contoh penggunaan


     ```html
     <!-- File index.html -->

     <!DOCTYPE html>
     <html>
       <head>
         <title>Website Pertamaku</title>
         <link rel="stylesheet" href="styles.css" />
       </head>
       <body>
         <h1>Website Pertamaku</h1>
         <p>Selamat Datang</p>
       </body>
     </html>
     ```
   ```css
     /* File styles.css */

     body {
       background-color: pink;
     }
     h1 {
       color: blue;
     }
     p {
       color: black;
     }
     ```
     hasilnya
        ![](ekstenal-css.jpg)

untuk syntax css sendiri,syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value.Penggunaan nya seperti ini:
  ```html
  <!-- Pada file HTML -->
<p>Hello world</p>
  ```

  ```css
  /* Pada file CSS */
p {
  color: blue;
}
  ```

Penjelasan :
- tag p adalah selector 
- color adalah property
- blue adalah value 

&nbsp;
>Box Model CSS
- Margin adalah area kosong setelah border,dan bersifat transparan,yang berfungsi untuk mengatur jarak antar elemen
- Padding adalah area kosong di antara konten dan border,berfungsi untuk mengatur jarak pada isi elemen
- Border adalah garis tepi yang membungkus padding dan konten.
- Content adalah value dari isi kita,seperti gambar,audio dll

&nbsp;
> Website Responsif
- Viewport adalah tampilan layar yang menampilkan suatu konten,cara mengatur viewport dengan menambahkan meta pada tag head 
 ```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Website Pertamaku</title>
  </head>
  <body>
    <h1>Hayii</h1>
  </body>
</html>
 ```
    width=device-width,digunakan untuk mengikuti layar device.
    initial-scale=1.0,digunakan untuk mengatur pembesaran dari halaman.

- Flexbox, menggunakan justify-content
``` html
<!DOCTYPE html>
<html>

<head>
	<style>
        html, body, #flex-container {
            height: 100%;
        }
		#flex-container {
			display: flex;
			flex-direction:row;
			justify-content: flex-start;
		}
		.flex-item {
			width: 100px;
			height: 100px;
			margin: 4px;
			background: #ec5453;
			font-size: 60px;
			color: white;
			text-align: center;
		}
	</style>
</head>

<body>
	<div id="flex-container">
		<div class="flex-item">1</div>
		<div class="flex-item">2</div>
		<div class="flex-item">3</div>
	</div>
</body>

</html>
```
 hasilnya semua konten nya akan berada di kiri
  <!DOCTYPE html>
<html>

<head>
	<style>
        html, body, #flex-container {
            height: 100%;
        }
		#flex-container {
			display: flex;
			flex-direction:row;
			justify-content: flex-start;
		}
		.flex-item {
			width: 100px;
			height: 100px;
			margin: 4px;
			background: #ec5453;
			font-size: 60px;
			color: white;
			text-align: center;
		}
	</style>
</head>

<body>
	<div id="flex-container">
		<div class="flex-item">1</div>
		<div class="flex-item">2</div>
		<div class="flex-item">3</div>
	</div>
</body>

</html>

sedangkan kalau menggunakan flex-end,konten nya akan berpindah ke kiri semua,dan jika center,konten nya akan berada ditengah,space-between akan memberi ruang pada setiap dua item yang bersebelahan,dan untuk space around,maka setiap konten akan memberi jaraknya
&nbsp;

## Algoritma
---
Secara definisi `algoritma` adalah suatu urutan dari beberapa langkah logis (masuk akal) dan sistematis (terurut) yang digunakan untuk menyelesaikan masalah tertentu.

- jenis2 algoritma : deskriptif, pseudocode, flowchart
### Pseudocode
Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu. Pseudocode merupakan suatu bahasa yang memungkinkan programmer untuk berpikir terhadap permasalahan yang harus dipecahkan tanpa harus memikirkan syntax dari bahasa pemrograman yang tertentu.

***Membuat Algoritma sederhana***

> Menghitung luas segitiga

Secara deskripsi dapat ditulis sebagai :
- membuat variabel untuk sisi alas segitiga
- membuat variabel untuk tinggi segitiga
- membuat variabel untuk rumus luas segitiga 
- menampilkan variabel luas segitiga

> Penulisan dengan Pseudocode :
```
Judul
Program luas_segitiga

Deskripsi
var alas, tinggi;

Implementasi

alas ← 100;
tinggi ← 64;
luas_segitiga ← 1/2* alas * tinggi;

print luas_segitiga;
```

```

STORE "alas" with any value
STORE "tinggi" with any value

STORE "luas_segitiga" with
CALCULATE 1/2 times "alas" times "tinggi"

DISPLAY "luas_segitiga"
```

> Penulisan menggunakan JavaScript
```
    let alas = 3;
    let tinggi = 6;
    let luas_segitiga = 1/2*alas*tinggi;
    console.log(luas_segitiga)

```
akan menghasilkan output : 9



## JS Dasar
---
***Javascipt*** adalah bahasa pemrograman komputer yang dinamis. Pada umumnya Javascipt digunakan pada web browser untuk menciptakan halaman web yang menarik, interaktif serta merapkan berbagai fungsi pada halaman web.

### Tipe Data pada Javascript

- ***number*** : tipe data yang mengandung semua angka termasuk angka desimal.
- ***string*** : grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya.
- ***boolean*** : tipe data yang hanya mempunyai 2 buah nilai (TRUE dan FALSE).
- ***null*** : tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
- ***undefined*** :tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Tipe data undefined biasanya didapat dari hasil kesalahan program (error), kelalaian programmer, dan tidak direncanakan.
- ***object*** : koleksi data yang saling berhubungan (related).


### Operator Javascript

1. ***Assignment Operator***
   Assignment operator digunakan untuk menyimpan sebuah nila pada variabel. Tanda operatoin ini adalah sama denga (=)

2. ***Mathematical Assignment Operator***
   Menggunakan gabungan tanda operator matematika dan sama dengan, misal +=, -= dan lain sebagainya.

3. ***Increment dan Decrement***
   Gunakan increment atau decrement untuk menambah atau mengurangi sebesar 1 nilai. Tanda operatormya adalah ++  atau --.

4. ***Arithmetic Operator***
   Arithmetic operator adalah operator yang melibatkan operasi matematika.
   - Tambah (+)
   - Kuramg (-)
   - Perkalian (*)
   - Pembagian (/)
   - Modulus (%)

5. ***Comparison Operator***
   Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara true or false
   
6. ***Simbol comparison operator***
   - Lebih kecil dari : <
   - Lebih besar dari: >
   - Lebih kecil atau sama dengan: <=
   - Lebih besar atau sama dengan: >=
   - Sama dengan: ===
   - Tidak sama dengan: !==


7. ***Logical Operator***
   Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman. Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE. Simbol dari Logical Operator adalah sebagai berikut:
   - AND operator (&&) : AND akan menghasilkan nilai true jika kedua atau semua premis bernilai TRUE.
   - OR operator (||) : OR akan menghasilkan nilai true jika salah satu premis mengandung nilai TRUE
   - NOT operator (!) : NOT akan membalikkan sebuah nilai BOOLEAN. TRUE menjadi FALSE dan sebaliknya.

### Conditional
Conditional merupakan statement percabangan yang menggambarkan suatu kondisi.

***IF ... ELSE IF ... STATEMENT***

Perkondisan remote control (menggunakan if else). Else … If statement dapat kita gunakan jika kita mempunyai berbagai kondisi.

```
let tombol = 4;

if (tombol === 1) {
    console.log('SCTV');
} else if (tombol === 2) {
    console.log('Indosiar');
}else if (tombol === 3) {
    console.log('Trans 7');
} else if (tombol === 4) {
    console.log('Trans TV');
} else {
    console.log('Channel tidak ditemukan');
}
```

***SWITCH CASE CONDITIONAL***

Switch case :digunakan untuk mempermudah ketika pengkodisian lumayan panjang/banyak
```
let tombol = 11;
switch(tombol) {
    case 1:
        console.log('SCTV');
        break;
    case 2:
        console.log('Indosiar');
        break;
    case 3:
        console.log('Trans 7');
        break;
    case 4:
        console.log('Trans TV');
        break;
    default:
        console.log('Channel tidak ditemukan');
}
```

***TRURHY AND FALSY***

Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.

```
let data = 'Data';

// cek data by truthy
if (data) {
    console.log('Data ini tidak kosong');
} else {
    console.log('Data kosong');
}
```


***TERNARY OPERATOR***

Ternary operator - kurang cocok untuk mengecek banyak kondisi -kalau lebih dari 3 disarankan pake if else
```
let makan = true;

makan ? console.log('sudah kenyang') : console.log('lapar');
```


### Looping

***FOR LOOP***

For loop  dapat digunakan ketika sudah tau batas awal dan akhir looping di angka berapa. Cara penulisan for :

> for (initialitation; condition; post-exression) { statement }

- Inisialisasi: Sebagai inisialisasi awal dari mana mulainya sebuah pengulangan. Kita memberikan nilai awal/default pada parameter ini
- Condition: For loop akan terus berjalan selama kondisi ini terpenuhi. Selama kondisi bernilai TRUE.
- Post-expression (Increment/Decrement): Iterasi statement yang digunakan untuk mengupdate variabel yang menjadi kontrol pada pengulangan

```
let angka = 1;
for (angka; angka <= 10; angka++) {
    console.log(angka);
}
```

***WHILE LOOP***

Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan. WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE.

> WHILE (expression) { statement }

```
let count = 1;
while (count <= 10 ) {
    console.log(count);
    count +=1;
}
```

***DO WHILE LOOP***

Do while cara penulisannya mirip seperti if statement tetapi kalau if statement hanya sekali atau tidak ada perulangan, maka do while akan diulang tetapi belum menegrti hasil dan titik akhirnya.

cara penulisan :

```
do {
    statement(s);
}while (expression;)
```

contoh penggunaan :
Angka yang dapat dibagi dengan 2,3,4,5,6 
```
let i = 1
let isKetemu = false

while (!isKetemu) {
    if (
        i % 2 == 0 &&
        i % 3 == 0 &&
        i % 4 == 0 &&
        i % 5 == 0 &&
        i % 6 == 0 
    ) {
        console.log(i);
        isKetemu = true
    }

    i++
}
```

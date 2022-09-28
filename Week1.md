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

## Algoritma dan Data Struktur
- perbedaan antara Algoritma dan Data Structures
- manfaat dari algoritma dan data structure
- membuat algoritma sederhana
- menerapkan algoritma ke dalam bahasa pemrograman
- memahami Big O Notation
- mempraktikkan pendekatan menyelesaikan suatu masalah untuk diselesaikan melalui program
- menerapkan salah satu algoritma dengan JavaScript
- menerapkan salah satu struktur data dengan JavaScript


## Javascript Dasar
- peran JavaScript pada web development
- menjalankan JavaScript
- membedakan berbagai tipe data
- menggunakan operator
- membedakan control flow (conditional dan looping)
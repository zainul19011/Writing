# Array Multidimensional
Array multidimensional adalah array dalam array
## Membuat array multidimensional
> ```
>let namaArray = [
> [elemen1, elemen2],
> [elemen3, elemen4],
>[elemen5, elemen6],
>];
contohnya
>
>``` js
>let inventory = [
>  ["Kaos Polos", 21],
>  ["Jaket Hoodie", 13],
>  ["Topi", 7],
>];
>
>console.log(inventory);
>/* Output:
>[
> ["Kaos Polos", 21],
> ["Jaket Hoodie", 13],
> ["Topi", 7],
>]*/
pada inventory diatas adalah array yang memiliki array didalam nya,dengan begitu inventory merupakan array multidimensional.

## Akses Array Multidimensional
cara mengaksesnya cukup panggil nomor indeks dan nomor kolom nya 
> namaArray[indexBaris][indexKolom];

contoh :
>
>``` js
>let inventory = [
>  ["Kaos Polos", 21],
>  ["Jaket Hoodie", 13],
>  ["Topi", 7],
>];
>
>console.log(inventory[0][0]); // Output: Kaos Polos
>console.log(inventory[2][0]); // Output: Topi
>console.log(inventory[1][1]); // Output: 13

## Array Multidemensi juga memiliki method dan property 
seperti array dimensi,beberapa diantar nya:
- .length yang berfungsi untuk mengembalikkan jumlah panjang array
- constructor berfungsi sebagai membuat prototipe objek array
- Prototype berfungsi untuk menambah objek atau methode baru kedalam array
- .push() method yang berfungsi untuk menambahkan item pada urutan terakhir di array
- .pop() method yang berfungsi untuk menghapus item pada urutan terakhir di array
- .shift() method yang berfungsi menghapus item pada urutan pertama di array

## Looping pada Array
- .for()
contohnya
>``` js
>let inventory = [
>  ["Kaos Polos", 21],
>  ["Jaket Hoodie", 13],
>  ["Topi", 7],
>];
>
>for (let i = 0; i < inventory.length; i++) {
>  for (let j = 0; j < inventory[i].length; j++) {
>    console.log(inventory[i][j]);
>  }
>}
>
>// Output:
>// Kaos Polos
>// 21
>// Jaket Hoodie
>// 13
>// Topi
>// 7

- .forEach(),looping pada setiap elemen
>``` js
>
>let inventory = [
>  ["Kaos Polos", 21],
>  ["Jaket Hoodie", 13],
>  ["Topi", 7],
>];
>
>inventory.forEach((baris) => {
> baris.forEach((kolom) => {
>    console.log(kolom);
>  });
>});
>
>// Output:
>// Kaos Polos
>// 21
>// Jaket Hoodie
>// 13
>// Topi
>// 7

- .map(),looping dengan membuat array baru
>``` js
>
>let inventory = [
>  ["Kaos Polos", 21],
>  ["Jaket Hoodie", 13],
>  ["Topi", 7],
>];
>inventory.map((baris) => {
>  baris.map((kolom) => {
>    console.log(kolom);
>  });
>});
>
>// Output:
>// Kaos Polos
>// 21
>// Jaket Hoodie
>// 13
>// Topi
>// 7

## Array Object
secara garis besar array object adalah kumpulan object yang seragam,objek yang berada dalam satu array dan memiliki properti yang sama,cara mengakses dengan menggunakan perulangan dari array,contohnya :
- for()
>``` js
>
>const fruits = [
>  {
>    name: "strawberry",
>    color: "red",
>    qty: 5
>  },
>{
>    name: "blueberry",
>    color: "blue",
>    qty: 10
>  },
>  {
>    name: "orange",
>    color: "orange",
>    qty: 5
>  },
>  {
>    name: "grape",
>    color: "purple",
>    qty: 2
> }
>];
>
>for(let i = 0; i < fruits.length; i++) {
>  console.log(fruits[i].name);
>}
>>
>// Output:
>// strawberry
>// blueberry
>// orange
>// grape

- .map()
>``` js
>const fruits = [
>  {
>    name: "strawberry",
>    color: "red",
>    qty: 5
>  },
> {
>    name: "blueberry",
>    color: "blue",
>    qty: 10
>  },
> {
>   name: "orange",
>    color: "orange",
>    qty: 5
> },
>  {
>    name: "grape",
>    color: "purple",
>    qty: 2
>  }
>];
>
>fruits.map(data => console.log(data.name));
>
>// Output:
>// strawberry
>// blueberry
>// orange
>// grape

# Rekursif
Rekursif adalah fungsi yang memanggil dirinya sendiri,dan pemanggilan ini yang disebut rekursif,rekursif digunakan untuk hal yang berhubungan dengan calculation,contohnya
>``` js
>function faktorial(n) {
>  if (n == 1) {
>   return 1;
>  } else {
>    return n * faktorial(n - 1);
>  }
>}
>
>console.log(faktorial(4))
>// Output:
>// 24
jika fungsi nya dijalankan,prosesnya akan seperti ini
>```
>4*faktorial(3) // faktorial(3) = 3*faktorial(2)
>4*3*faktorial(2) // faktorial(2)= 2*faktorial(1)
>4*3*2*faktorial(1) //faktorial(1) = 1 --> masuk ke kondisi n==1
>sehingga didapatkan hasil
>4*3*2*1=24

#  Asynchronous
Asynchronous adalah perintah yang mengizinkan komputer kita untuk melakukan proses perintah yang lain,kita bisa melakukan proses sekaligus(multi-thread),beberapa proses asynchronous pada javascript :
- setTimeout(function, milliseconds) digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali,contohnya
>``` js
>setTimeout(() => {
>  console.log("Cuci baju"); // proses asynchronous
>}, 1000);
>console.log("Menyapu");
>console.log("Mengepel");
>console.log("Memasak");
>
>// 1000 ms = 1 second
>
>// Output:
>// Menyapu
>// Mengepel
>// Memasak
>// Cuci baju

- setInterval(function, milliseconds) digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan,contohnya 
>``` js
> setInterval(() => {
>  console.log("Cuci baju"); // proses asynchronous
>}, 3000);
>console.log("Menyapu");
>console.log("Mengepel");
>console.log("Memasak");
>
>// 3000 ms = 3 second
>
>// Output:
>// Menyapu
>// Mengepel
>// Memasak
>// Cuci baju (x time)
>
>// Cuci baju akan dijalankan setiap 3 detik sekali

## Promise
- contoh penggunaan promise fullfiled menggunakan .then()
>
>``` js
>const condition = true;
>
>let newPromise = new Promise((resolve, reject) => {
>  if (condition) {
>    // apa yang dilakukan jika promise 'fulfilled'
>    resolve("Berhasil");
>  } else {
>    // apa yang dilakukan jika promise 'rejected'
>    reject(new Error("Error Gagal"));
>  }
>});
>
>newPromise.then((result) => {
>  return result;
>})
>.then((result2) => {
> console.log(result2 + "!!"); // Output: Berhasil!!
>});
>
keterangan 
>   - resolve(), jika proses berhasil
>   -   reject(), jika proses gagal

- Contoh penggunaan promise rejected,untuk mengantisiapasi terjadi nya error kita bisa menambahkan .catch() pada promise.
>``` js
>const condition = false;
>
>let newPromise = new Promise((resolve, reject) => {
>  if (condition) {
>    // apa yang dilakukan jika promise 'fulfilled'
>    resolve("Berhasil");
>  } else {
>    // apa yang dilakukan jika promise 'rejected'
>    reject(new Error("Error Gagal"));
>  }
>});
>
>newPromise.then((result) => {
>  console.log(result);
>})
>.catch((error) => {
>  console.log(error.message); // Output: "Error Gagal"
>});

- Ada juga penggunaan .finally(),yang berfungsi sebagai callback yang pasti tereksekusi baik dalam konidisi apapun,baik fullfield ataupun rejected,contoh penggunaan
>``` js
>const condition = true;
>
>let newPromise = new Promise((resolve, reject) => {
>  if (condition) {
>    // apa yang dilakukan jika promise 'fulfilled'
>    resolve("Berhasil");
>  } else {
>    // apa yang dilakukan jika promise 'rejected'
>    reject(new Error("Error Gagal"));
>  }
>});
>
>newPromise
>  .then((result) => {
>    console.log(result); // Output: Berhasil
>  })
>  .catch((error) => {
>    console.log(error);
>  })
>  .finally(() => {
>    console.log(
>      "Finally tetap terpanggil dalam kondisi fulfilled ataupun rejected"
>    ); // Output: Finally tetap terpanggil dalam kondisi fulfilled ataupun rejected
>  });

# Web Storage
## Cookie 
cookie adalah data yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah,dengan maks data yang disimpan 4096 bytes (4 KB).
## Local Storage dan Session Storage
local dan session storage memiliki maks data yang lebih besar yaitu 5mb
- local storage memiliki karakteristik yaitu:
  - Menyimpan data tanpa tanggal kadaluarsa.
  - Data tidak akan dihapus ketika web browser ditutup dan   akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
  - Dapat menyimpan data hingga 5MB.
  - Hanya dapat menyimpan data string. 

- Session storage mempunyai beberapa karakteristik, yaitu:
  - Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
  - Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
  -  Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
  - Data yang tersimpan dalam session storage harus berbentuk string.
  - Hanya dapat menyimpan data sebanyak 5MB.

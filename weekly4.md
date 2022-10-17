# Asynchronous-Fetch
Proses Fetch adalah salah satu proses asynchronous di javascript sehingga kita perlu menggunakan promise atau async/await.

## Fetch dengan promise
contoh request data dengan fetch menggunakan promise
>``` js
>fetch("https://jsonplaceholder.typicode.com/posts")
>  .then(function (response) {
>    return response.json();
>  })
>  .then(function (post) {
>    console.log(post);
>  });
kita menggunakan endpoint api dari <u>JSONPlaceholder</u>,tampilan dari console log nya adalah
<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/asynchronous-fetch-get-data.png" alt="console.log" />

## Fetch dengan async/await
contoh request data dengan fetch menggunakan async/await
>``` js
>const tesFetchAsync = async () => {
>  let response = await fetch("https://jsonplaceholder.typicode.com/posts");
>  response = await response.json();
>  console.log(response);
>};
>tesFetchAsync();
hasilnya:
<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/asynchronous-fetch-get-data.png" alt="console.log" />

# Asynchronous-Async/await
- async, mengubah function synchronous menjadi 
- asynchronous.
await, menunda eksekusi hingga proses asynchronous selesai.

## Async
Penggunaan nya:
>
>``` js
>// async menggunakan keyword function 
>async function tesAsyncAwait() {
>  return "Fulfilled";
>}
>
>console.log(tesAsyncAwait());
>// async menggunakan arrow function
>const tesAsyncAwait = async () => {
>  return "Fulfilled";
>};
>
>console.log(tesAsyncAwait());

hasilnya:
<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/asynchronous-async-01.png" alt="console.log" />

## Await

Await hanya bisa digunakan dalam async function dan await adalah keyword dalam async yang digunakan untuk menunda hingga proses asynchronous selesai.contoh penggunaan
>``` js
>// Definisikan dahulu promise yang ingin digunakan
>let condition = true;
>let tesAsyncAwait = async (condition) => {
>  if (condition) {
>    return "Condition is fulfilled!";
>  } else {
>    throw "Condition is rejected!";
>  }
>};
>
>
>// Membuat fungsi run menjadi asynchronous menggunakan async/await
>const run = async (condition) => {
>  try {
>    const message = await tesAsyncAwait(condition);
>    console.log(message);  // Output: Condition is fulfilled!
>    console.log("After condition is fulfilled"); // Output: After condition is fulfilled
>  } catch (error) {
>    console.log(error);
>  }
>};
>
>run(true);
>
kode di atas, kita dapat melihat bahwa run adalah sebuah fungsi async dan await dipanggil bersamaan dengan fungsi tesAsyncAwait(condition). await pada fungsi ini artinya, console.log pada message dan After condition is fulfilled tidak akan dijalankan (ditunda) hingga proses tesAsyncAwait(condition) selesai dijalankan.,hasilnya
<img src="https://skilvul-assets-01.s3-ap-southeast-1.amazonaws.com/lesson/js-intermediate/asynchronous-await-01.png" alt="console.log" />  


## GitHub Lanjutan

### Kolaborasi membuat organizations

- masuk ke akun github anda
- klik `setting` -> `organizations` -> `new organizations`
- pick a plant yang diinginkan atau free
- set up your organization

## Responsive Web
- Bertujuan membuat desain website kita dapat diakses dalam device apapun
- Cara untuk membuat web responsive bermacam-macam :
  1. meta viewport
  2. max-width
  3. relative unit
  4. media query
  5. flex
  6. grid
### meta viewport
- Viewport : area web yg dapat diakses oleh user
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />  //ini adalah meta viewport
    <title>Document</title>
  </head>
```
- tetapi, Cara dengan viewport kurang efektif/responsive
### max-width
>```html
><!-- File index.html -->
>//menambah gambar agar responsive
><img src="responsive.jpg" alt="">

> ```css
> /* File styles.css */
> img{
> width: 100%;
>}  //maka output gambar, akan sebesar 100% dari layar

### relativ unit
- macam-macam relative unit, diantaranya :
  1. em : relative pada ukuran huruf parent terdekatnya
>    ```html
>    <!-- File index.html -->
>      <p class="rem">hallo ini dari rem</p>

> ```css
> /* File styles.css */
>    .em {
>      font-size: 2em;
>    } //maka output font-size em = sebesar 40px

  2. rem: relative pada ukuran huruf dari root element
    - Ukuran root html, kebanyakan 16px
> ```html
><!-- File index.html -->
>   //index.html
>    <p class="em">hallo ini dari em</p>

> ```css
> /* File styles.css */
>    //style.css
>    .rem {
>    font-size: 2rem;
>    } //maka, output dari font 2 rem ini = sebesar 32px 

  3. vw: ukuran tinggi dari viewport
    - 1vw = 1% dari ukuran viewport
  4. vh : mengatur tinggi layar
  5. % : mengambil ukuran parentnya
### Media query
- Media query : mengatur beberapa styling tegantung pada jenis device tertentu
- Media query => @media ()
> ```css
>@media (max-width: 600px ) {
>   .menu {
>     display: none;
>    }

## Bootstrap 
Boostrap adalah framework HTML, CSS, dan JavaScript yang berfungsi untuk mendesain website responsive dengan cepat dan mudah.Diciptakan pada tahun 2011 oleh Mark Otto dan Jacob Thornton dari Twitter

Kegunaan Boostrap

- Membuat website mobile friendly
- memudahkan resize gambar
- menambahkan halaman tanpa ribet
- membuat website interaktif

contoh menggunakan nya
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <link rel="stylesheet" href="style.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3" crossorigin="anonymous"></script>
  </head>
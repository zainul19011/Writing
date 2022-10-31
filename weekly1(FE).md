# WEEK 1 - Front End Bootcamp
## React Dasar

### React js
- Reactjs adalah sebuah Library javascript yang dapat digunakan untuk membantu pembuatan website disisi frontend, React Js dibuat dan dikembangkan oleh Facebook(sekarang menjadi META).React Berbasis Virtual DOM dan setiap element yang dibuat dengan react disebut React Component.React memiliki format '.jsx' untuk javascript dan '.tsx' untuk typescript.Javascript biasanya hanya bisa berjalan di web browser dengan bantuan HTML
- Dengan adanya **NodeJS** maka javascrpit bisa berjalan diluar browser,NodeJS bisa digunakan untuk mendownload package yang disediakan React
- Selain React ada juga alternatif lain seperti Angular, Vue, dan Svelte
- _Berbasis komponen_ = Dengan React kita bisa membuat asset komponen yang bisa dipake berulang kali
_(cth : Membuat navbar cukup sekali untuk beberapa page, jika ada perubahan cukup ubah di main navbarnya aja nanti yang lain ikut keupdate)_
- di dalam `div id="root"` kita menyisipkan halaman halaman yang dibutuhkan
- React hanya bisa return 1 element maka harus dibungkus dengan `<div>` atau fragment kosong `<>`
- Setiap membuat component nama functionnya harus capital diawal  (function **Home**())
- import **file** from **'.folder/file'**

```
function Home (){
 return (
   <div> 
      <h1> Hallo </h1>
   </div>
 )
}

export default Home
```

- `Class` dalam JSX ditulis `ClassName`
- Untuk memberhentikan npm bisa menggunakan `ctrl + c` atau `npm kill-host 300`


#### Instalisasi React

- ada berbagai cara untuk menggunakan React didalam project kita, dan yang paling mudah adalah dengan menggunakan template yang telah dicustom oleh react yaitu create-react-app atau CRA.
- berikut langkah menginstall react js dengan CRA - pastikan telah menginstall Nodejs - buka terminal dan pilih root folder - ketik npx create-react-app my-app (my-app sebagai nama folder) - tunggu sampai proses install selesai - setelah itu buka folder react di vscode dan kita bisa melihat susunan file react.

### React Component

- Didalam sebuah react kita dapat membuat sebuah component seperti element html dengan menggunakan function
- react component memiliki beberapa kelebihan diantarnya - reusable / dapat digunakan berkali-kali - readable / lebih mudah dibaca - panjang kode menjadi lebih pendek dan rapih sehingga memudahkan proses debugging.
- Untuk membuat component perlu membuat folder `component` dulu yang isinya menampung banyak component
- `state` adalah data yang ada di dalam component
- `props` adalah data yang dikasih yang nanti akan diterima mirip ketika memberi attribute <br/>
  _(data **state** dikasih ke dalam **props**)_ 
- Terdapat component `stateless` yang berarti tidak memiliki data yang dinamis
- Untuk bisa menggunakan component harus dipanggil dulu `import nama from "./nama.css";`
- Menggunakan single tag ketika memanggil component di file utama`<navbar/>`
- Lalu di dalam template component panggil dengan `{props.namaproperty}`
- Nama property adalah isi data yang ingin ditampilkan menggunakan component (data yang ingin dicustom di component)
- Langkah menggunakan component
	- Membuat folder component & buat file component yg ingin dibuat menggunakan `.jsx`
	- Buat template componentnya (jangan lupa nama componentnya menggunakan capital di depannya)
	- Di file JSX utama misalnya `App.jsx` tulis import component dan tulis letak filenya (import..from..)
	- Sisipkan nama property dari component menggunakan single tag dan isi props atau attribute data
	  `<card nama="tata" umur="18"/>`
	- Di file component tulis di parameter function `(props)`
	- Panggil data props dengan memanggil `{props.nama}`
- contoh cara membuat react component
>```js
>      export deafult const Card = () =>{
>          return(
>              <div>
>                  <h1>Ini adalah sebuah card component</h1>
>              </div>
>          )
>      }
>
  note: nama component harus diawali huruf kapital

- cara menggunakan react component hampir sama dengan cara menggunakan element html, hanya kita perlu melakukan import terlebih dahulu

> ``` js
>     import Card from 'component/card';
>
>      export default const Home = () =>{
>         return(
>              <>
>                  <Card/>
>              </>
>          )
>      }
>
### React Lifecycle

- Lifecycle didalam react memiliki tiga alur utama

- **Mounting** adalah sebuah siklus pertama ketika aplikasi dibuka.
- **Update** adalah sebuah siklus ketika terjadi perubahan data.
- **Unmount** adalah siklus setelah komponen dibuka.

- sebelum versi 16 atau adanya Hooks untuk memanipulasi Lifesycle didalam React harus menggunakan
  - componentDidMount();
  - componentWillUpdate();
  - componentWillUnMount();
- sedangkan untuk versi 16/ setelah Hooks sampai sekarang kita dapat menggunakan useEffect() untuk menghandle Lifecycle didalam React.
- Ada 2 cara membuat component yaitu dengan **class** dan **function**, dan yang akan kita pakai adalah function karena lebih sederhana sedangkan class adalah cara classic
- Kita bisa menambahkan side effect pada proses lifecycle menggunakan function serta callback `useEffect(() => {}` dengan menyisipkan `import {useEffect} from "react";`
- Jadi side effect ini berlaku ketika component ini menjalankan lifecyclenya sampai selesai dan auto berjalan ketika halaman dimuat
- Dalam VS code proses ngebacanya itu = function paling atas - mount pada return - baru side effect _(urutannya si side eefect di skip dulu, mount diduluin)_
- Ketika state ada yang berubah maka semua proses rendering diulang lagi dr awal seperti refresh
- Dapat menggunakan depedency berupa`[]` jika side effect ingin berlaku cukup sekali ketika mount saja tanpa berlaku ketika ada update
- `npm install axios` sebagai pengganti fetch
- Dengan menggunakan axios tidak perlu lagi menggunakan `.then` 2 kali dan tidak perlu merubah jadi json
- Hooks ditandai dengan function `use..`

## React Lanjutan

### React Hooks

- **React Hooks** adalah Fitur yang memungkinkan untuk menggunakan state dan fitur React lainnya tanpa menuliskan sebuah kelas. Hooks menggunakan konsep Functional Component.

- untuk menggunakan Hooks harus menggunakan React versi 16.8 atau diatasnya

- ada beberapa Hooks yang disediakan oleh react, berikut hooks yang paling populer dan sering digunakan
  - **useState()** adalah hook yang digunakan untuk membuat dan memanipulasi sebuah state.
  - **useEffect()** adalah hook yang digunakan untuk menghandle lifecycle.
  - **useRef()** adalah hook untuk memanipulasi elemen DOM.
  - **useContext** adalah hook untuk memanipulasi sebuah Context API.
  - dll
- cara menggunakan hooks kita harus mengimport terlebih dahulu dari react

  ```
      import {useState} from 'react';

      export default const Home = () =>{
          const [name, setName] = useState('Randi')

        return(
            <>
                <p> nama saya  {}</p>
            </>
        )
    }

    //output: nama saya Randi

  ```
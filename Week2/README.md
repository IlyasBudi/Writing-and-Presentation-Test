## Writing Test Week 2
## Day 1: Javascript Scope & Function
#### Javascript Scope
- Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
- Ada 2 macam scope dalam javascript yaitu global scope dan local scope.
- Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.
Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. Contoh:
```
Let myName = “Raisha”;
Function greeting() {
   Return myName;
}

Console.log (myName);
```
- Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.
- Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks. Contoh:
```
Function greeting () {
       Let myName “Raish.
a”;
       Return myName;
}
Console.log (greeting())
Console.log (myName);
```
- Blocks adalah code yang berada didalam curly braces {}. Conditional, function, dan looping menggunakan blocks.
#### Javascript Function
- Function adalah sebuah code blok dalam sebuah grup untuk menyelesaikan 1 task/
- Membuat function
```
function greeting() {
    return 'Hello World' ;
};
```
- Memanggil function
```
greeting()
console.log(greeting());
```
#### argumen dan parameter function
- Argumen: adalah nilai yang digunakan saat memanggil function. 
- Jumlah argumen harus sama dengan jumlah parameternya. Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen. Contohnya:
```
function penambahan(a,b){
   return a + b;
}
console.log(penambahan(5,5))
```
- Parameter: berfungsi untuk menerima sebuah inputan data yang digunakan untuk melakukan task. 
- Contoh parameter:
```
function penambahan(a, b){
  return a + b;
}
```
#### Default parameter
- Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function.
- Contohnya:
```
function warnaKesukaan(warna = "putih"){
    return "Warna kesukaan saya adalah " + warna;
}
console.log(warnaKesukaan);
```
#### arrow function
- Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version). Contohnya:
```
hello = () => {
  return "Hello World!";
}
```
#### Short Syntax Function
- Single Line Block
``const sumNumbers = number => number + number ;``
- Multi Line Block
```
const sumNumbers = number => {
    const sum = number + number;
    return sum;
}
```
## Day 2: Data Type Built in Prototype & Method
## Tipe Data
- Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
Tipe data akan otomatis dideteksi oleh JavaScript saat variabel tersebut diberikan suatu nilai.
- Ada 6 tipe data di JavaScript. Kelima diantaranya merupakan tipe data primitif dan satu non-primitif, yaitu:
1.	String: deretan karakter yang diapit oleh sepasang tanda kutip.
2.	Number: bilangan bulat, pecahan, dan lain-lain.
3.	Boolean: nilai benar dari sebuah pernyataan yang dituliskan sebagai true atau false.
4.	Null: sebuah nilai yang berarti kosong atau menunjuk pada nilai yang tidak ada.
5.	Undefined: menandakan kondisi variabel yang belum diberi sebuah nilai.
6.	Object (non-primitif): sebuah kumpulan pasangan properti dan nilai.
- Perbedaan tipe data primitif dan non-primitif:
- Perbedaan paling mendasar antara keduanya pada JavaScript adalah tipe data primitif memiliki sifat immutable dan tidak memiliki properties sementara tipe data non-primitif bersifat mutable dan memiliki properties.
## PROTOTYPE AND METHOD
#### String
##### Property<br />
  - Length: Digunakan untuk mengetahui panjang karakter pada string.
##### Method<br />
  - toUpperCase(): Digunakan untuk mengubah string menjadi huruf besar.<br />
  - toLowerCase(): Digunakan untuk mengubah string menjadi huruf kecil.<br />
  - charAt() Digunakan untuk mengembalikan karakter sesuai dengan index yang dipanggil.<br />
  - Includes(): Digunakan untuk mencari apakah suatu substring berada dalam suatu string. Return value dari method ini adalah true atau false.<br />
  - Split(): Digunakan untuk membagi string menjadi array substring, dan mengembalikan array baru.
#### Number
##### Property
  - MAX_VALUE
  - MIN_VALUE
  - NaN
##### Method
  - isInteger(): Digunakan untuk menentukan apakah suatu nilai merupakan integer atau tidak, memiliki dua keluaran yaitu true atau false.
  - isNaN(): Digunakan untuk menentukan apakah suatu nilai merupakan NaN (Not-A-Number) dan akan mengembalikan dua nilai yaitu true dan false.
#### Math
##### Property
- Math.E               // Bilangan Euler
- Math.LN2             // Log 2 
- Math.LN10            // Log 10
- Math.LOG2E           // Log E di Basis 2
- Math.LOG10E          // Log E di Basis 10
- Math.PI              // Pi
- Math.SQRT1_2         // Akar Kuadrat dari 0.5
- Math.SQRT2           // Akar Kuadrat dari 2
#####	Method
- Math.abs(x): Digunakan untuk mengubah angka x yang bernilai negatif menjadi positif.
- Math.pow(x, y): Digunakan untuk menghitung hasil dari x pangkat y.
- Math.cbrt(x): Digunakan untuk menghitung akar pangkat 3 dari x.
- Math.round(x): Digunakan untuk membulatkan angka desimal x menjadi bilangan bulat.
- Math.floor(x): Digunakan untuk membulatkan angka desimal x ke bawah.
- Math.ceil(x): Digunakan untuk membulatkan angka desimal x ke atas.
- Math.random(): Digunakan untuk menampilkan angka secara acak antara 0 hingga 1 (0 termasuk. 1 tidak).
- Math.max(x, y, z, ..., n): Digunakan untuk mencari angka terbesar di antara parameter x, y, z, ..., n.
- Math.min(x, y, z, ..., n): Digunakan untuk mencari angka terkecil di antara parameter x, y, z, ..., n.

## Day 3,4,5: DOM
- DOM adalah singkatan dari (Document Object Model). Ini dalah sebuah interface yang memungkinkan Anda sebagai developer untuk memanipulasi style, konten dari sebuah website.
- Dengan adanya DOM ini, JavaScript diberi akses untuk membuat HTML menjadi dinamis, seperti:
    - Mengubah element HTML pada halaman website.
    - Mengubah attribute HTML pada halaman website.
    - Mengubah CSS style pada halaman website.
    - Menambah dan/atau menghapus element maupun attribute HTML.
    - Menambah HTML event.
    - Berinteraksi dengan semua HTML event di website.
- Di HTML DOM, semua element HTML dari sebuah website dianggap sebagai objek. Dan sama seperti objek JavaScript pada umumnya, objek element HTML di HTML DOM juga mempunyai properti dan method atau yang lebih dikenal dengan istilah DOM Property dan DOM Method.
- Jadi untuk mengubah nilai properti dari element HTML, kita bisa menggunakan DOM Property dan untuk memanggil fungsi dari suatu element HTML, kita bisa menggunakan DOM Method
## Mengakses Element HTML
- getElementById(id)<br />
Digunakan untuk mengakses element HTML berdasarkan nilai id-nya.
- getElementsByTagName(tag)<br />
Digunakan untuk mengakses element-element HTML berdasarkan jenis tag-nya.
- getElementsByClassName(className)<br />
Digunakan untuk mengakses element-element HTML berdasarkan nilai attribute class-nya.
- querySelectorAll(cssSelector)<br />
Digunakan untuk mengakses element-element HTML berdasarkan CSS Selector-nya HTML.
- Children<br />
Method yang digunakan untuk mengakses semua elemen anak dari elemen saat ini.
- parentElement<br />
Method yang digunakan untuk mengakses elemen induk dari elemen saat ini.
## Manipulasi DOM
- createElement: Digunakan untuk membuat elemen HTML pada suatu website.
- innerHTML: Digunakan untuk menampilkan data pada elemen tertentu berdasarkan “id” elemen tersebut.
- InnerText: Digunakan untuk menampilkan konten berupa teks di halaman website.
- append(): Digunakan untuk menambahkan element baik berupa object node maupun DOMString.
- appendChild(): Hanya bisa menambahkan Node Object tapi tidak bisa untuk menambahkan elemen berupa DOM String
- Remove: Digunakan untuk menghapus element html pada website.
- getAttribute(): Digunakan untuk mengembalikan atribut element.
- setAttribute(): Digunakan untuk menetapkan atribut dari suatu element.
- .style.color: digunakan untuk mengatur warna pada suatu element.
- .style.backgroundColor: Digunakan untuk mengatur warna background suatu element.
- classList: Digunakan untuk memanipulasi class yang ada pada element HTML.
## DOM Event
- DOM Events merupakan object model yang bertugas untuk membantu interaksi user dengan document HTML.
- Contoh HTML DOM events
    - Click
    - Scroll
    - Change
    - Focus
    - Hover
    - Submit
    - Blur
- Menangkap Interaksi User
    - Element.addEventListener("event)
    - Element.onevent
- EventListener <br />
  Dengan menggunakan Element.addEventListener("event") dapat menerapkan beberapa hal yaitu :
    - Bisa dihilangkan
    - Bisa ada beberapa event listener yang sama untuk 1 element
    - Memiliki argument tambahan {options}
- Contoh EventListener :
  - EventListener - Click 
    `` <input id="user-input"/> ``
    `` <button id="alert-button">show</button> ``
    Memanggil element berdasarkan id
    `` const input = document.getElementById("user-input") ``
    `` const button = dosument.getElementById("alert-button") ``

    ```
     button.addEventListener("click", function()) {
      alert(input.value)
    } 
    ```
- EventListener - Blur : event dimana sebuah element kehilangan fokus dari user 
- Contoh EventListener - Blur <br />
  Misalkan saat ingin memvalidasi isi dari ``<input id = "username" />`` agar panjangnya minimal 6 karakter

  `` const input = document.getElementById("username") ``

  ```
  input.addEventListener("blur", () => {
    if(input.value.length < 6) alert("Panjang username minimal 6")
  })
  ```
- EventListener - Form Submission
- Contoh EvenListener - Form Submission <br />
  Misalkan terdapat beberapa input dalam sebuah form `` <input name="email"/> `` dan ``<input type="password" name="password"/>`` <br />
  Untuk mendapatkan isi dari kedua inputan tersebut terdapat 2 cara :
  - Memasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut
  - Memasang event listener di form, lalu gunakan FormData untuk menggambil data dari masing-masing input
  ``` 
    const form = document.getElementById("form")

    form.addEventListener("submit", function(event)){
    event.preventDefault()

    const formData = new FormData(form)
    const values = Object.fromEntries(formData) {
      email: ....
    }
  })
  ```

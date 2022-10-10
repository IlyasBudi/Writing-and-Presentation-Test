## Writing Test Week 3
## Array dan Array Multidimensional
### Array
- Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya.
- Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
- Contoh array:
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
console.log(buah);
```
#### Mengakses Array
- Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0. Contohnya:
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
console.log(buah[2]); //output: pisang
```
#### Update Array
- Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array. Contohnya:
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
buah[0] = “jeruk”;
console.log(buah);
// output: [“jeruk”, “semangka”, “pisang”]
```
#### Const dalam array
- Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
- Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.
#### Array properties
- Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer. Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
#### Array method
- Array memiliki method atau biasa disebut built-in methods. Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
- Contoh array build in method:
- .push(): adalah method untuk menambahkan item  array pada urutan yang paling akhir.
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
buah.push(“jeruk”)
console.log(buah); //output: [“mangga”, “semangka”, “pisang”, “jeruk”]
```
- .pop(): adalah method yang menghapus item array index terakhir.
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
buah.pop()
console.log(buah); //output: [“mangga”, “semangka”]
```
- .shift() adalah method untuk menghapus item Array pada index pertama.
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
buah.shift()
console.log(buah); //output: [“semangka”, “pisang”];
```
- .unshift(): adalah method untuk menambahkan item Array pada index pertama.
```javascript
let buah = [“mangga”, “semangka”, “pisang”];
buah.unshift(“jeruk”)
console.log(buah); //output: [“jeruk”, “mangga”, “semangka”, “pisang”]
```
#### looping pada array
- Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach().
- .forEach() adalah method untuk melakukan looping pada setiap elemen array.
```javascript
let cars = ['mangga', 'semangka', 'pisang'];
cars.forEach(element => {
console.log(element);
}); 
```
- .map() melakukan perulangan/looping dengan membuat array baru.
```javascript
let arr = [1,2,3,4,5];

let doubled = arr.map(num => {
    return num * 2;
});
console.log(doubled);
```
- Perbedaannya adalah .forEach tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping, Lalu dari segi performance juga sangat jauh.
- Jadi, gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database. Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.
### Array Multidimensional
- Multidimensional Array bisa dianalogikan dengan array of array.
- Multidimensional ini seperti table. Baris pada table itu menunjukan jumlah array, Column pada table itu menunjukan isi dari tiap array.
- Contohnya:
```javascript
let arrMulti = [
  ["Nama", "ilyas"],
  ["Umur", 20],
  ["alamat", "tangerang"],
];
Console.log(arrMulti);
```
- Mengakses multidimensional array
```javascript
let arrMulti = [
  ["Nama", "ilyas"],
  ["Umur", 20],.
  ["alamat", "tangerang"],
];
console.log(arrMulti[0][1]);
```
- Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.
## Object
- Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method).
- Properti adalah data lengkap dari sebuah object. Sementara Method adalah action dari sebuah object.
- Membuat object
```javascript
let person = {
    name: "ilyas",
    umur: 20,
};
```
#### Mengakses object
```javascript
let person = {
    nama: "ilyas",
    umur: 20,
};
console.log(person.nama); //output: “ilyas”
```
- Bracket Notation: Kita juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object. Contohnya:
```javascript
let person = {
    nama: "ilyas",
    umur: 20,
};
console.log(person['nama']);
```
#### Update property object
```javascript
let person = {
    nama: "ilyas",
    umur: 20,
};
person.nama = "ilyas budi"
console.log(person['nama']); //output: “ilyas budi”
```
#### Delete property object
```javascript
let person = {
    nama: "ilyas",
    umur: 20,
};
delete person.umur;
```
#### Method
- Jika value yang kita masukkan pada property berupa function. Maka itu disebut method.
- Console adalah global javascript object. log adalah properti yang berupa function dari object console.
- Nested object
```javascript
let buku = {
  judul: "Harry Potter",
  tahun: 1997,
  penulis: {
      nama: "J.K. Rowling",
      umur: 57,
      negara: "inggris",
  },
};

console.log(buku);
console.log(buku.penulis.nama);
```
#### Looping object
- Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping. Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.
#### Array of object
- Object sama seperti Array yang bisa menyimpan banyak data. Kita dapat menggunakan array of object untuk data yang lebih dari satu.
## Recursive
- Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
- Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
- Struktur recursive:
```javascript
function recursive() {
  // ...
  recursive();
  // ...
}
```
Ciri ciri recursive:<br />
1. Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.<br />
2. Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.
- Contoh kasus recursive menghitung mundur number:
```javascript
function countDown(fromNumber) {
console.log(fromNumber);

let nextNumber = fromNumber - 1;

//jika kondisi bernilai false maka recursive berhenti
if (nextNumber > 0) {
    countDown(nextNumber);
};
countDown(3)
//Output
// 3
// 2
// 1
```
## Asynchronus
- Asynchronous yang biasa dikenal juga dengan sebutan non-blocking mengizinkan komputer kita untuk memproses perintah lain sambil menunggu suatu proses lain yang sedang berlangsung. Ini artinya kita bisa melakukan lebih dari 1 proses sekaligus (multi-thread). Eksekusi perintah dengan asynchronous tidak akan melakukan blocking atau menunggu perintah sebelumnya selesai. Jadi sambil menunggu kita bisa mengeksekusi perintah lain.
- Jika JavaScript secara default bersifat synchronous, maka bagaimana jika ingin menerapkan proses asynchronous ? Ada beberapa cara untuk membuat proses asynchronous.
- Menjalankan Asyncrhonus pada javascript bisa menggunakan:
1.	``setTimeout(function, milliseconds)`` digunakan untuk simulasi pemanggilan kembali proses asynchronous yang sedang/sudah selesai dijalankan. Pemanggilan hanya dilakukan 1 kali.
2.	``setInterval(function, milliseconds)`` digunakan untuk simulasi pemanggilan proses asynchronous yang sedang/sudah dijalankan dalam interval waktu tertentu. Pemanggilan dilakukan berkali-kali sesuai interval waktu yang ditentukan.
- asynchronous lebih effisien dibandingkan synchronous. Namun, permasalahan terjadi saat menggunakan asynchronous, ada satu perintah yang bergantung pada output eksekusi asynchronous sebelumnya. Dengan kata lain fungsi berjalan kejar-kejaran (race condition), sehingga data yang kita inginkan menjadi kosong.
- Untuk mengatasi masalah tersebut, kita dapat menggunakan:
1.	callback<br />
2.	promise<br />
3.	async / await
#### Callback
- Callback adalah sebuah function, namun bedanya dengan function pada umumnya adalah pada cara eksekusinya.
- Contoh Penggunaan Callback pada Asynchronous
```javascript
function p1() {
    console.log('p1 done')
  }

    function p2(callback) {
    setTimeout(
    function() {
    console.log('p2 done')
      callback()
    },100
    )
  }

  function p3() {
  console.log('p3 done')
  }
  p1()
  p2(p3)
  ```
#### Promise
- Asynchronous - Promise merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason)
  ```javascript
    function GetUser(id) {
    return new Promise((resolve, reject) => {
    if (id !== "" && id !== undefined) {
      reesolve (id);
    } else {
      reject ("ID Harus di Isi");
        }
    });
    }
    
    GetUser( ) 
    .then((response) => {
    console.log(response);
     })
     .catch((error) => {
    console.log(error);
    });
  ```
## Web Storage
- Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.
#### Cookies
- Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
- Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu.
- Namun ada beberapa kekurangan yang perlu kita perhatikan mengenai cookies di antaranya:<br />
1.	Setiap kita mengakses situs web, cookies juga kembali dikirim sehingga memperlambat aplikasi web kamu dengan mengirimkan data yang sama.<br />
2.	Cookies disertakan pada setiap HTTP request, sehingga mengirimkan data yang tidak dienkripsi melalui internet, maka saat kita ingin menyimpan data dalam cookies kita harus mengenkripsinya terlebih dahulu.<br />
3.	Cookies hanya dapat menyimpan data sebanyak 4KB.<br />
4.	Lalu cookies juga memiliki tanggal kadaluarsa. Tanggal ini telah ditentukan sehingga web browser bisa menghapus cookies jika tanggal sudah kadaluarsa atau tidak dibutuhkan.
#### Local Storage
- LocalStorage merupakan salah satu cara yang dapat digunakan untuk menyimpan data di web browser.
- Local storage memiliki karakteristik sebagai berikut:<br />
1.	Menyimpan data tanpa tanggal kadaluarsa.<br />
2.	Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.<br />
3.	Dapat menyimpan data hingga 5MB.<br />
4.	Hanya dapat menyimpan data string.
- Untuk menyimpan data pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter.
```javascript
localStorage.setItem('key', value);
```
- Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter.
```javascript
localStorage.getItem('key');
```
- Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter.
```javascript
// menghapus key tertentu
localStorage.removeItem("key");

// menghapus semua key
localStorage.clear();
```
#### Session Storage
- Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir.
- Session storage mempunyai beberapa karakteristik, yaitu:<br />
1.	Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.<br />
2.	Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.<br />
3.	Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.<br />
4.	Data yang tersimpan dalam session storage harus berbentuk string.<br />
5.	Hanya dapat menyimpan data sebanyak 5MB.
- untuk menyimpan data pada session storage adalah sebagai berikut:
```javascript
// menambah session storage
sessionStorage.setItem('key', value);
```
- Untuk mendapatkan data dari session storage juga menggunakan getItem(), seperti berikut ini:
```javascript
// mendapatkan session storage
sessionStorage.getItem('key');
```
- Syntax untuk menghapus data dari session storage ada 2, yaitu:
// menghapus session storage satu persatu berdasarkan key
```javascript
sessionStorage.removeItem('key');

// menghapus seluruh session storage sekaligus
sessionStorage.clear();
```

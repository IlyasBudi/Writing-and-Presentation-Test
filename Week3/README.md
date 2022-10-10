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
## Array Multidimensional
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
